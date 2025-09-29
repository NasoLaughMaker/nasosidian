```ruby
# config/initializers/sidekiq.rb (例)

Sidekiq.configure_server do |config|
  config.redis = { url: "redis://#{ENV['KVS_HOST']}:6379/#{ENV.prefix_fetch('SIDEKIQ_REDIS_DB', 8)}" }
  config.default_job_options = { retry: 5 }

  # ここを修正します
  # 環境変数に応じて切り替えたい場合は、このまま if/else 構造を使用
  # 今回はファイル出力のみなので、直接パスを指定
  config.logger = Sidekiq::Logger.new(Rails.root.join('log', "sidekiq.log"))
  config.logger.level = Logger::INFO
end
```
