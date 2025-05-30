memo

🛑 初回プッシュ時のエラー内容
```sh
bin/rails db:test:prepare test test:system
  shell: /usr/bin/bash -e {0}
  env:
    RAILS_ENV: test

##[debug]/usr/bin/bash -e /home/runner/work/_temp/b601b4fb-46e7-45bd-afb0-8349435ab91d.sh

/home/runner/work/rails_test_sample/rails_test_sample/db/schema.rb 
doesn't exist yet. 
Run `bin/rails db:migrate` to create it, then try again. 
If you do not intend to use a database, you should instead alter /home/runner/work/rails_test_sample/rails_test_sample/config/application.rb to limit the frameworks that will be loaded.
```
- `bin/rails db:migrate`してから `git push`
  
  
📁 testディレクトリの構成
```sh
$ tree ./test
test
├── application_system_test_case.rb # システムの基底クラス
├── controllers                     # コントローラに対する機能テストディレクトリ
│   └── todos_controller_test.rb
├── fixtures                        # テストデータ(fixtures)を管理するディレクトリ
│   ├── files
│   └── todos.yml
├── helpers                         # ヘルパークラスに対するテストディレクトリ
├── integration                     # 複数のコントローラ間でのテストに関するテストディレクトリ
├── mailers                         # Action Mailerに対するテストディレクトリ
├── models                          # モデルに対するテストディレクトリ
│   └── todo_test.rb
├── system                          # システムテストディレクトリ
│   └── todos_test.rb
└── test_helper.rb                  # ユニットテストで読み込むテスト用ヘルパークラス
```

🧪 ディレクトリごとのテスト観点：
 - modelsディレクトリのテスト：モデルに対するテスト
 - channelsディレクトリ：Action Cableに関するテスト
 - systemディレクトリ：アプリケーション全体を結合して動作を検証するE2Eテストであるシステムテスト
 - controllerディレクトリ：アプリケーションの各機能を結合して検証するテスト

