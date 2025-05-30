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
├── application_system_test_case.rb
├── controllers
│   └── todos_controller_test.rb
├── fixtures
│   ├── files
│   └── todos.yml
├── helpers
├── integration
├── mailers
├── models
│   └── todo_test.rb
├── system
│   └── todos_test.rb
└── test_helper.rb
```

🧪 ディレクトリごとのテスト観点：
 - modelsディレクトリのテスト：モデルに対するテスト
 - channelsディレクトリ：Action Cableに関するテスト
 - systemディレクトリ：アプリケーション全体を結合して動作を検証するE2Eテストであるシステムテスト
 - controllerディレクトリ：アプリケーションの各機能を結合して検証するテスト

