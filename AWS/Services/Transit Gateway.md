複数のVPCや複数のオンプレミスネットワークを相互に接続するハブ機能を持つサービス。

## VPCピアリングとの違い

- VPCピアリングは1対1なのに対して、複数のVPC同士をひとつのハブで相互に接続できる。

## Transit Gatewayアタッチメント

Transit Gatewayが接続するリソースの窓口の総称

- VPCアタッチメント
    - 対象：VPC
    - ENI
        - ENIを作成する際にはTGW用のプライベートサブネットを作成することが推奨されている。
        - 一つのプライベートサブネット内でENIを作成し、ルートテーブルに定義をしたらVPC全体でTGWを使用可能。
- Direct Connecアタッチメント
    - 対象：オンプレミス
    - Direct Connect Gateway
- Site-to-Site VPNアタッチメント
    - 対象：オンプレミス
    - カスタマーゲートウェイ
- Peeringアタッチメント
    - 対象：他リージョンのTGW
    - TGW同士の直接接続
- Outpostアタッチメント
    - 対象：AWS Outposts（オンプレのAWS環境）
    - OutpostsのネットワークをTGWに接続

## アプライアンスモード