# libre-blue-os ビルドツール
## 概要
libre-blue-osでは、MX Linuxが公開しているビルドツール`build-iso-mx`のカスタム版を使用しています。

## ビルドと環境構築
### 環境構築
1. ビルドに必要なパッケージをインストールします。
   - `sudo apt install debootstrap syslinux-utils zsync expect git xorriso mkisofs genisoimage binutils`
### ビルド
1. 任意のディレクトリ(空で無くとも良い)で以下のコマンドを実行し、GitHubからリポジトリのソースコードを取得します
   - 最新版のみビルドする場合: `git clone --depth 1 https://github.com/ISnow-Systems/libre-blue-os.git`
   - 過去のバージョンに遡ってビルドする場合: `git clone https://github.com/ISnow-Systems/libre-blue-os.git`
     - 特定のタグ・ブランチでビルドする場合: `git clone -b <branch> https://github.com/ISnow-Systems/libre-blue-os.git`
2. `cd libre-blue-os`を実行してカレントディレクトリを変更します
3. `sudo ./build-iso -0` を実行してビルドを開始します。
   - オプション`-0`は処理を最初から行う場合に実行します
   - 中断地点からの継続を行う場合はここに**0**以外の数値を入力します。

## ライセンス
本ソースコードはGPL 3.0の条件に従い公開されています。  
ライセンスは[こちらから](https://github.com/ISnow-Systems/libre-blue-os/tree/master/LICENSE)ご確認いただけます。
