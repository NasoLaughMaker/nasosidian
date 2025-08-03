# CloudFormation

# S3バケットを削除したい

ACFを用いてS3バケットを削除する際、バケット内のオブジェクトが残っていたらバケットの削除が行えないという仕様がある。

対処法：

- オブジェクトを全削除するLambda関数を実装し、カスタムリソースとしてACFスタックに統合する。
- カスタムリソースに、S3バケットのリソースを指すDependsOn属性を設定する
    - DependsOn属性：実行する処理を、他のリソースの処理が完了するまで待つように制御できる。

# IAMリソースを作成・変更したい

CloudFormationでIAMリソースを作成するときは、作っていいよと明示しなければならない。それが `CAPABILITY_IAM` と `CAPABILITY_NAMED_IAM` 。IAMリソースは非常に強力なので、 CloudFormationが勝手に作らないように明示する必要がある。

| フラグ名 | 意味 | 使う場面 |
| --- | --- | --- |
| `CAPABILITY_IAM` | IAMリソースに自動で名前をつけて作成することを許可 | 一般的なIAMロールやポリシーの自動作成時 |
| `CAPABILITY_NAMED_IAM` | IAMリソースに指定した名前をつけて作成することを許可 | IAMロールの名前をテンプレート内で明示する場合 |

# Outputs

CFテンプレートの中の特別な場所で、スタックの結果として得られる重要な情報（VPC ID、S3バケット名など）を出力する場所。CFスタックの作成後にマネジメントコンソールやCLIで出力値を確認できる。

## Fn::InportValue

ACFにおける組み込み関数の一つ。別のCFスタックでExportされた値をインポートするための関数。

### 何ができる？

スタック間でリソース情報（VPC ID、サブネットID、セキュリティグループIDなど）を共有することができる。これにより、大規模なインフラを小さなスタックに分割して管理しやすくする。

**提供側**

```yaml
Outputs:
  VPCId:
    Description: "Export Security Group ID"
    Value: !Ref MySecurityGroup
    Export:
	    Name: SharedSecurityGroupID
```

**受け取り側**

```yaml
Resources:
  MyInstance:
    Type: AWS::EC2::Instance
    Properties:
      SecurityGroupIds:
        - !ImportValue SharedSecurityGroupID
```

`!ImportValue` ：YAMLにおける短縮記法（推奨）

`Fn::ImportValue` ：標準の形式

# cfn-signalヘルパースクリプト

Amazon EC2 インスタンスが正常に作成または更新されたかどうかを示すシグナルを CloudFormation に送信します。インスタンスにソフトウェアアプリケーションをインストールして設定する場合、ソフトウェアアプリケーションが使用できる状態になった時に CloudFormation にシグナルを送信できます。

![スクリーンショット 2025-07-20 16.34.06.png](スクリーンショット_2025-07-20_16.34.06.png)

## CloudFormationサービスロール

CFnにユーザーに代わってスタック内のリソースを呼び出すアクセス権限を許可するIAMロール。デフォルトではCFnはユーザー認証情報からスタック操作に対して作成される一時的セッションを使用する。

以下で `MyCloudFormationExecutionRole` を渡すことを許可できる。

```yaml
{
  "Effect": "Allow",
  "Action": "iam:PassRole",
  "Resource": "arn:aws:iam::123456789012:role/MyCloudFormationExecutionRole"
}
```