# Docker on texlive

## Directory
```
main - 論文
summary - 梗概
```

## HOW TO
実行にはdocker必須
buildに10-30分かかります。
```bash
docker build -t lualatex_image .
docker compose up -d
```

vscode拡張機能`Dev Container`のインストール。

vscodeの左下`><`アイコンから`実行中のコンテナにアタッチ`を選択。コンテナを選んだ後に、拡張機能`LaTeX Workshop`のインストール。

`/root`をマウントして`main(論文)`, `summary(梗概)`ディレクトリで作業を行う。