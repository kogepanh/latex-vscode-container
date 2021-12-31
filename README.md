<h1 align="center">LaTex for VS Code Remote - Container</h1>

<p align="center">Visual Studio Code Remote - Containers を利用してローカル環境を汚さずに LaTex を使用するためのサンプルです</p>

<div align="center">
<img src="https://img.shields.io/github/license/kogepanh/latex-vscode-container" />
<br />
<img src="https://img.shields.io/github/stars/kogepanh/latex-vscode-container" />
<img src="https://img.shields.io/github/issues/kogepanh/latex-vscode-container" />
<img src="https://img.shields.io/github/v/release/kogepanh/latex-vscode-container" />
<br />
<a href="https://hub.docker.com/r/korosuke613/ubuntu-texlive-ja-devcontainer" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/docker/image-size/korosuke613/ubuntu-texlive-ja-devcontainer/latest" /></a>
<a href="" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/github/repo-size/kogepanh/latex-vscode-container" /></a>
</div>

---

## 環境構築

下記のソフトウェアをインストールしてください。

- Docker
- Visual Studio Code
- VS Code 拡張機能
  - [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) (ms-vscode-remote.remote-containers)

## 実行

### 1. リポジトリを作成＆クローン

1-1. `Use this template` からリポジトリを作成してください。

![Use this template](https://user-images.githubusercontent.com/49851726/120323239-46418180-c320-11eb-9e46-a97217f18dc8.png)

1-2. `git clone [リポジトリのURL]` でプロジェクトをクローンしてください。

![Clone repository](https://user-images.githubusercontent.com/49851726/120324086-2d859b80-c321-11eb-9a3b-96d863eadf12.png)

### 2. VS Codeで `latex-vscode-container` を開く

### 3. Remote - Containers を実行する

ダイアログがサジェストされた場合はそこから実行できます。  
左下の `><` アイコンを押して、 `Open in Container (Remote Containers)` を実行することも可能です。

![Open in containers](https://user-images.githubusercontent.com/49851726/120071402-287adf00-c0ca-11eb-93fa-d678df2cfb02.gif)

### 4. Tex ファイルをビルドする

![Build Tex file](https://user-images.githubusercontent.com/49851726/120071423-552ef680-c0ca-11eb-8550-ddc877ee0150.gif)

### 5. ホットリロードされるのでリアルタイムに変更を監視できます

![Hot-reload](https://user-images.githubusercontent.com/49851726/120071435-6415a900-c0ca-11eb-9bf0-71e3df79f35f.gif)

---

## Options

### 複数プロジェクトを共存させたい人向け

ディレクトリを複数作成すればよいです。本サンプルでは `src` ディレクトリのみが存在していますが、以下のようにフォルダ名を変更しても問題なく動きます。

```txt
.
├── .devcontainer
├── .gitignore
├── .vscode
├── project1
│   ├── img
│   ├── resume.tex
│   ├── style
│   └── thesis.tex
└── project2
    ├── img
    ├── resume.tex
    ├── style
    └── thesis.tex
```

### ホットリロードがウザイ人向け

Tex ファイルが大きくなったきた時など、ホットリロードを止めたい人もいるかと思います。そういう人は `.vscode/settings.json` を以下のように編集してください。

```settings.json
-  "latex-workshop.latex.autoBuild.run": "onFileChange"
+  "latex-workshop.latex.autoBuild.run": "never",
```

選択肢には以下の3通りがあります

- `onFileChange` : 依存関係にあるファイルの変更を検知した時
- `onSave` : tex ファイルを vscode で保存した時
- `never` : ホットリロードしない

### コマンドでビルドすることも可能です

```bash
latexmk [filename].tex
```

---

## License

[MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2021 kogepan
