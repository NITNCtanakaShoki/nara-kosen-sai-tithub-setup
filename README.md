# 奈良高専祭 2023 情報工学科展 TitHubのSetup

## 概要

以下のチュートリアルを行うためのSetupになります。

- [初級: 飾り文字](https://tithub.tech/creaft/nara-kosen-sai-beginner)
- [中級: カーソルを置くと動くボタン](https://tithub.tech/creaft/nara-kosen-sai-intermediate)
- [上級: ](https://tithub.tech/creaft/nara-kosen-sai-advanced)

## Install Git

### for macOS

macの場合は`git`と言うツールがすでにインストールされているため、特にすることはありません。`ターミナル`と言うアプリを開いて

```shell
git --version
```

とコマンドを打ち込んでバージョンが表示されればOKです。

### for Windows

Windowsの場合は`git`が最初からインストールされていないため、[http://git-scm.com/download/win](http://git-scm.com/download/win)にアクセスしてGitをインストールしてください

`Git Bash`というアプリを開いて

```shell
git --version
```

とコマンドを打ち込んでバージョンが表示されればOKです。

## Install Node.js

NodeJSがインストール済みでない場合は、[https://nodejs.org/en/download](https://nodejs.org/en/download)からNodeJSをインストールしてください。

Windowsであれば、`Windows Installer (.msi) 64-bit`をダウンロードしてインストールしてください。

macOSであれば、`macOS Installer (.pkg)`をインストールしてください。

ターミナルまたはGit Bashを開いて

```shell
node --version
```

でバージョン確認ができればOKです。

## Git clone

プロジェクトをローカルコピーします。
GitBashやターミナルを開いて以下のコマンドでローカルコピーしてください。

```shell
cd Desktop # デスクトップに移動
git clone https://github.com/NITNCtanakaShoki/nara-kosen-sai-tithub-setup
```

## Install VScode

VScodeなどのエディターをインストールしてください。VScodeは[https://code.visualstudio.com/download](https://code.visualstudio.com/download)からダウンロードできます。

VScodeを開いたら、`Svelte for VS Code`と言う拡張機能をインストールしてください。

[拡張機能のインストール方法](https://learn.microsoft.com/ja-jp/power-pages/configure/vs-code-extension)

## プロジェクトをVSコードで開く

VScodeを開きます。アプリを起動してフォルダーを選択するか、ターミナルやGitBashで以下のコマンドを入力してください

```shell
cd Desktop/nara-kosen-sai-tithub-setup # プロジェクトに移動
code . # VScodeで開く
```

## プロジェクトのサーバーの実行

ターミナルまたはGitBashで以下のコマンドを実行してください。

```shell
cd Desktop/nara-kosen-sai-tithub-setup # プロジェクトに移動
npm install # 依存関係をインストール
npm run dev # サーバーを立ち上げる
```

## ブラウザでアクセスする

ChromeやEdge、Safariなどで[http://localhost:5173](http://localhost:5173)にアクセスしてください。

## エラーが出る場合

### NodeJSのバージョン不足

以下のようなエラーがnpm installで出る場合

```shell
npm WARN read-shrinkwrap This version of npm is compatible with lockfileVersion@1, but package-lock.json was generated for lockfileVersion@3. I'll try to do my best with it!
 
npm ERR! code ENOTSUP
npm ERR! notsup Unsupported engine for @sveltejs/kit@1.27.3: wanted: {"node":"^16.14 || >=18"} (current: {"node":"14.17.5","npm":"6.14.14"})
```

NodeJSのバージョンが古い可能性があります。NodeJSのバージョンを上げてください

```shell
npm install -g n
n stable
```

バージョンが上がっていなければターミナルやVScodeを再起動してみてください
