# CIができているかのテスト
- Reactを使用
- Firebaseにデプロイ

## 参考サイト
[React × Firebase × Gitlabで自動デプロイ(CI/CD)を構築する](https://zenn.dev/hisasy/articles/cea64d233ba538)

[firebaseにデプロイする方法](https://zenn.dev/hisasy/articles/ec057b18566215)

ルートディレクトリに.gitlab-ci.ymlを配置

現在はビルド、デプロイのステージのみ記載

##　CIのオプション
- マージリクエストのときのみこのステージを実行したいとき
    ```bash
    only:
        - merge_requests
- ジョブのアーティファクトが生成されてから自動的に削除されるまでの時間を設定
    ```bash
    expire_in: 1 hour # 一時間で削除することで不要なアーティファクトがストレージを占有するのを防ぐ