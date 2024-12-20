# ベースとなるDockerイメージ指定
FROM ubuntu:latest

# タイムゾーンの設定
ENV TZ=Asia/Tokyo
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# 必要なパッケージのインストール
RUN apt-get update && apt-get install -y \
    sudo \
    git \
    vim \
    curl \
    wget \
    tar

# # TeX Liveのダウンロード
# RUN wget http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz

# # TeX Liveの展開
# RUN tar -xzf install-tl-unx.tar.gz

RUN sudo apt install texlive-full -y

# RUN code --install-extension James-Yu.latex-workshop

# 作業ディレクトリの設定
WORKDIR /root

RUN mkdir -p /root/.vscode/
COPY .vscode /root/.vscode