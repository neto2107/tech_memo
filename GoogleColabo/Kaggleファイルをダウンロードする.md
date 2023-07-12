# GoogleColabでKaggleデータセットを扱う手順

```Py
#kaggleライブラリのインストール
!pip install kaggle

#ローカルから、Colab上にkaggle.jsonをアップロード
from google.colab import files

uploaded = files.upload()

for fn in uploaded.keys():
  print('User uploaded file "{name}" with length {length} bytes'.format(
      name=fn, length=len(uploaded[fn])))

!mkdir -p ~/.kaggle/ && mv kaggle.json ~/.kaggle/ && chmod 600 ~/.kaggle/kaggle.json

#データセットを指定してダウンロード
!kaggle datasets download -d xhlulu/huggingface-bert
```

