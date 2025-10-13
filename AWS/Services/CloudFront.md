CDN(コンテンツデリバリーネットワーク)サービス。世界中のエッジロケーションに配置されたサーバーを利用して、コンテンツを高速に配信可能。

## CloudFrontディストリビューション

特定のコンテンツデリバリーの設定や構成を指す。特定のオリジン(通常はS3バケット、EC2、API Gatewayなど)からデータを取得し、キャッシュ。リソースを使う時に最初に設定する。作成するとコンテンツにアクセスするためのURLが作成される。

- キャッシュTTL
    - Time to Liveの略でキャッシュの更新頻度を設定できる。

## 複数のオリジンを設定する

静的コンテンツをS3から、動的リクエストをALBから取得する。また、WAFを設定する。

### S3側の設定

OAC（オリジンアクセスコントロール）を作成し、CFディストリビュージョンに追加。S3バケットポリシーを更新し、OACへのアクセスのみを許可する。

### ALB側の設定

ALBにカスタムヘッダーを要求し、WAFで検査するように設定。

WAFでカスタムヘッダーの存在を検証するルールでルールでWeb ACLを作成し、ALBに関連付ける。

## CloudFrontとカスタムオリジン間の通信でHTTPSを必須にする
CloudFrontのキャッシュ動作をHTTTPS要求に設定し、CloudFrontオリジンのプロトコルポリシーを「Match Viewer」に設定することで、強力な暗号化を使用して機密データを保護できる。（[参考](https://docs.aws.amazon.com/ja_jp/AmazonCloudFront/latest/DeveloperGuide/using-https-cloudfront-to-custom-origin.html)）

1. ディストリビューションで、「Origin Protocol Policy」設定を変更する。
2. オリジンサーバーにSSL/TLS証明書をインストールする。（S3オリジン、または特定のその他のAWSオリジンを使用する場合は不要。）