# scikit-mobility
## 位置情報データを使って可視化することや、人の動きを解析することができる。
### データの型はTrajDataFrameとFlowDataFrameがある。
#### TrajDataFrame

・latitude: 緯度

・longitude: 経度

・datetime: 日時

#### FlowDataFrame

・origin: 起点

・destination: 終点

・flow:  フロー

が必要である。

人流データを可視化することで

１都市計画への活用

２移動パターンの特定

3イベントの効果測定

などが解析可能である。

## TrajDataFrameの作り方

```
import skmob
data_list = [[1, 36.984094, 135.549136, '2020-7-5 10:42:05'], 
             [1, 36.984198, 135.549222, '2020-7-5 10:42:20'], 
             [1, 36.984224, 135.549424, '2020-7-5 10:51:00'], 
             [1, 36.984211, 135.549370, '2020-7-5 10:58:43']]
tdf = skmob.TrajDataFrame(data_list, latitude=1, longitude=2, datetime=3)

```
## TrajDataFrameの可視化
```
tdf.plot_trajectory(zoom=10, weight=3, opacity=0.5, tiles='OpenStreetMap')

```

zoom: 地図をの大きさで出力するか

weight: 地図上に出力する線の太さを指定

opacity: 地図上に出力する線の透過度を指定

tiles: 地図を選択を指定

