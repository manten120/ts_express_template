# npm package のメモ

- `typescript` TypeScriptをコンパイルするtscコマンドをつかうために必要

- `typesync` 型定義パッケージを自動でインストールする

- `jest` テストを行う

- `ts-jest` コンパイルせずTSのままテストを行えるようにする

- `supertest` テストの際にHTTPリクエストをシミュレートする

- `ts-node-dev` TSをコンパイルせずに実行する。ホットリロードする。

- `http-errors` ステータスコードに応じてエラーを作成してくれる

- `typeorm` データベースをTypeScriptで操作する

- `reflect-metadata` typeormを使うときに必要。デコレーター(@)と関係してる?。

- `mysql2` typeormでMySQL8と接続するときに必要。mysqlではダメ

## ESLint, Prettier関連のnpmパッケージ

- `eslint` varをconstにしたり、関数定義をアロー関数に統一したりしてくれる

- `prettier` 行末のセミコロンやインデントを担当

- `@typescript-eslint/eslint-plugin` ESLintでTypeScriptを扱えるようにする

- `@typescript-eslint/parser` @typescript-eslint/eslint-pluginをつかうために必要

- `eslint-config-airbnb-base` JavaScriptのコーディングルール

- `eslint-plugin-import` import, exportの記法に対応する

- `eslint-plugin-prefer-arrow-functions` 関数定義をアロー関数に統一する

- `eslint-config-prettier` prettierと競合するESLintのルールをオフにする。TypeScriptに関するルール(@typescript-eslint/eslint-plugin)にも対応

- `eslint-import-resolver-typescript` TypeScriptでimport文のパスを解決する

- `eslint-plugin-jest` Jestに関するESLintルール
