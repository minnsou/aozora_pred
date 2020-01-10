## OverView

青空文庫の作品を使って作者推定を行ってみた。大きな流れは以下。

1. wgetを使って青空文庫から本文をダウンロード
1. MeCabを使って、本文を整形
1. Doc2Vecを使って、本文をベクトル化（本文から作られたベクトルをx、作者IDをyとした教師データの作成）
1. kerasを使ってニューラルネットを構成し、分類問題として教師あり学習

コードをある程度詳しく解説した記事を[qiita](https://qiita.com/minnsou/items/37e3155c92103dae04f4)で書きました。一緒にご覧ください。

Mac OS Catalina 10.15.2を使用しています。Windowsでちゃんと動くかどうかは未確認。

## Description

- aozora_pred.ipynb モデル構築や学習を行う実際のファイル。上から実行するだけ。

- authors.txt ダウンロードする著者が書いてあるファイル。人数が多くなかったので今回は手作業で作ったが、今後拡張したい人はこれを自作しても良い。

- data 青空文庫からダウンロードしてきたhtmlファイル等を保存するディレクトリ。

## Requirement

BeautifulSoup, gensim, numpy, matplotlib, keras, MeCab

## Usage

`git clone git@github.com:minnsou/aozora_pred.git`して、aozora_pred.ipynbを上から順に実行してください。
