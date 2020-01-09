青空文庫の作品を使って作者推定を行ってみた。大きな流れは以下。

1. wgetで本文をダウンロード
1. MeCabを使って、本文を整形
1. Doc2Vecを使って、本文をベクトル化（本文から作られたベクトルをx、作者IDをyとした教師データの作成）
1. kerasを使ってニューラルネットを構成し、分類問題として教師あり学習