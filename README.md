# <p align="center">LaTex for VS Code Remote - Container</p>

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

## 事前準備

下記のソフトウェアをインストールしてください。

- git（なくてもなんとかなるが…笑）
- Docker
- Visual Studio Code
- VS Code 拡張機能
  - [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
  - [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

## 環境構築

1. `git clone https://github.com/kogepanh/latex-vscode-container.git`
2. VS Codeで `latex-vscode-container` を開く。
3. 左下の `><` アイコンを押して、 `Open in Container (Remote Containers)` を実行する。
4. 待つ。
5. 完了！

## 実行

## build

```bash
latexmk sample.tex
```

`sample.pdf`という実行ファイルができているはず。
