# Elastic Load Balancing(ELB)

- トラフィックを自動で分散する負荷分散器。

## Application Load Balancer(ALB)

- HTTPやHTTPSに対応する単一のロードバランサ―。L7で機能。アプリ側で認証のロジックを考慮しなくても、Cognito等を使ってALB側で認証してくれる。唯一ホストベースのルーティングに対応。
    - ホストベース
        - FQDNで振り分け
    - パスベース
        - 「フラグメント」や「クエリ文字列」を除いたドメイン名以降の部分で振り分け
- 送られてきたリクエストを別のURLにリダイレクトできる。
    - HTTPで送られたリクエストをHTTPSに変換など。

## Network Load Balancer(NLB)

- TCP/UDPのトラフィックを負荷分散。大量のアクセスが想定されるアプリケーションで推奨。L4で機能。固定IPアドレスの割り当てが可能。
- WAFの割り当てができないため、固定IPを使いたいがWAFも割り当てたい場合はGlobal Accelaratorを使う

## Gateway Load Balancer(GWLB)

- サードパーティー仮想アプライアンスを簡単にデプロイ、スケーリング、管理できる。L3のゲートウェイ機能とL4の負荷分散機能を備えている。

## Classic Load Balancer(CLB)

- EC2インスタンスの負荷分散。ほとんどはALBとNLBでカバーできるが、特殊なケースで利用。
    - EC2-Classicのアプリケーション
    - TCP/SSLリスナーの設定が必要
    - Cookieを使用したスティッキーセッション