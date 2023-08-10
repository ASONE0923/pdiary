# Pdiary

## サービス概要
Pdiaryは、毎日の出来事や気持ちを簡単に記録できる日記アプリケーションです。日常の小さな出来事や、その日感じたことを瞬時にキャッチして保存することができます。
- ログイン画面
[![Image from Gyazo](https://i.gyazo.com/549714c57a1e6e8ba296af4e4f4830cc.png)](https://gyazo.com/549714c57a1e6e8ba296af4e4f4830cc)
- 投稿画面
[![Image from Gyazo](https://i.gyazo.com/0c0586b6c400e2d5d81813b43ce7fa3d.jpg)](https://gyazo.com/0c0586b6c400e2d5d81813b43ce7fa3d)

## 想定されるユーザー層
日常の出来事や感情を簡単に記録し、後で振り返りたいと考える20代から40代の男女。特に日記を書く習慣があるが、紙の日記帳よりもデジタルで手軽に記録したいと考える層。

## 使用技術
- Ruby 3.2.2
- Rails 7.0.6
- MySQL (gem: mysql2 0.5)
- Puma Web Server 5.0
- Sprockets-Rails
- Devise 4.8.0
- Bootsnap

## サービスコンセプト
* ユーザーが日常の出来事や感情を簡単に、しかも素早く記録できるアプリが欲しかった。
* 紙の日記帳を持ち歩くのは不便であり、スマホで簡単に日記をつけられるサービスが求められていた。
* どんな場所でも、どんな時間でも気軽に日記をつけられるサービスを目指している。
* デザインのシンプルさや、ユーザーの気持ちを直感的に色や絵文字で表現できる点が強み。

## 実装を予定している機能
### MVP
* 会員登録
* ログイン
* 日記の記録
* 日記の閲覧
* 日記の検索

### その後の機能
* 気持ちや天気を絵文字での入力サポート
* フォト日記機能
* トピックタグ付け機能
* プライバシーモード (特定の日記を非公開にする)
* シェア機能 (SNS等での共有)

## Dockerを使ってのローカル環境構築手順

### 前提条件

- Dockerがインストールされている
- Docker Composeがインストールされている

### 手順

1. リポジトリをクローンする

```bash
git clone [リポジトリのURL]
cd [リポジトリ名（ディレクトリ名）]
```

2. Dockerイメージをビルドする

```bash
docker-compose build
```

3. データベースを作成・マイグレーションを実行する

```bash
docker-compose run web rails db:create db:migrate
```

4. アプリケーションを立ち上げる

```bash
docker-compose up
```

5. ブラウザでアプリケーションにアクセスする

通常、[http://localhost:3000](http://localhost:3000) にアクセスすることでアプリケーションが表示されます。

### その他のコマンド

- 依存ライブラリ（gemなど）を追加した場合:

```bash
docker-compose build
```

- データベースのマイグレーションを実行する場合:

```bash
docker-compose run web rails db:migrate
```

- アプリケーションを終了する場合:

```bash
docker-compose down
```

