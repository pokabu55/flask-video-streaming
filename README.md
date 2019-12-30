flask-video-streaming
=====================

Supporting code for my article [video streaming with Flask](http://blog.miguelgrinberg.com/post/video-streaming-with-flask) and its follow-up [Flask Video Streaming Revisited](http://blog.miguelgrinberg.com/post/flask-video-streaming-revisited).

***
### 以下、自分で追記分です

# 参考サイト
1. [リアルタイムで顔にモザイクを掛ける](https://tech.fusic.co.jp/posts/2019-12-03-2019-12-03-put-mosaic-on-human-faces/)
   * 最初はここを参考にした
   * 2019のクリスマスんアドベントカレンダーなので、記事自体は新しく、中身も大丈夫そう。
2. [Flask: カメラ動画・ストリーミング配信やってみた♬](https://qiita.com/MuAuan/items/31830ad8036df5f1f732)
    * 2018年のQiitaの記事
    * ３に書いているflaskを用いたストリーミングの、必要ライブラリの詳細が書かれてる
    * その他、FPSの実験も実施している
3. １，２が参照しているストリーミングの[リポジトリ](https://github.com/miguelgrinberg/flask-video-streaming)
    * フォークしました（ここがフォークです）

# 実行前に
* 必要ライブラリの確認
  * OpenCVを使う場合は、直下のディレクトリにある requirements-opencv.txt を参照のこと
  * 上記リストのバージョンを問わず、ライブラリ名だけでpip3でインストール。
  * app,py の下記を修正することで、カメラからの画像を表示できる
```
# 修正前
from camera import Camera
```
```
＃ 修正後
from camera_opencv import Camera
```

  * 修正前は、予め用意された3枚のjpgが順に表示されるのみ

* [こっちの記事](https://qiita.com/MuAuan/items/92f3b1004cfde071add6)が必要そう
