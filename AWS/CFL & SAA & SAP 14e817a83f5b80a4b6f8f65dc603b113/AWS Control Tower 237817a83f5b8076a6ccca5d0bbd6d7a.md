# AWS Control Tower

## 新しいAWSアカウントをControl Towerに自動で登録する方法

1. 新しいAWSアカウントにAWSControlTowerExecutionロールを作成し、AWS Control Tower管理者アカウントがロールを引き受けることができるようにロールを設定する。
2. 新しいAWSアカウントの詳細を使用して、AWS Service Catalog ProvisionProduct APIオペレーションを呼び出す。
    1. AWS Control Towerは内部的に「AWS Service Catalog」を使用して、新しいアカウントのプロビジョニングを実行する。
        1. Account Factory for Terraform
        2. Landing one Account Factoryなど