
## cloudwatch

### get-metric-statistics

* --unit
  取得したいメトリクスの単位を指定してデータをフィルタリングする
  CloudWatchでは、一つのメトリクス名に対して異なる単位（例：BytesとMegabytes）でデータが保存されている可能性があるため、
  どの単位の統計を取得するかを明示する必要がある

| 分類              | 指定する値 (Unit) | 説明                             | 
| ----------------- | ----------------- | -------------------------------- | 
| 時間              | Seconds           | 秒                               | 
|                   | Microseconds      | マイクロ秒                       | 
|                   | Milliseconds      | ミリ秒                           | 
| データ量 (バイト) | Bytes             | バイト                           | 
|                   | Kilobytes         | キロバイト                       | 
|                   | Megabytes         | メガバイト                       | 
|                   | Gigabytes         | ギガバイト                       | 
|                   | Terabytes         | テラバイト                       | 
| データ量 (ビット) | Bits              | ビット                           | 
|                   | Kilobits          | キロビット                       | 
|                   | Megabits          | メガビット                       | 
|                   | Gigabits          | ギガビット                       | 
|                   | Terabits          | テラビット                       | 
| 割合・個数        | Percent           | パーセント                       | 
|                   | Count             | 個数                             | 
| データ転送速度    | Bytes/Second      | バイト/秒                        | 
|                   | Kilobytes/Second  | キロバイト/秒                    | 
|                   | Megabytes/Second  | メガバイト/秒                    | 
|                   | Gigabytes/Second  | ギガバイト/秒                    | 
|                   | Terabytes/Second  | テラバイト/秒                    | 
| 通信速度・頻度    | Bits/Second       | ビット/秒                        | 
|                   | Kilobits/Second   | キロビット/秒                    | 
|                   | Megabits/Second   | メガビット/秒                    | 
|                   | Gigabits/Second   | ギガビット/秒                    | 
|                   | Terabits/Second   | テラビット/秒                    | 
|                   | Count/Second      | 回数/秒                          | 
| その他            | None              | 単位なし（カスタムメトリクス等） | 

  * 指定する際の注意点
    保存されているメトリクスの単位と、リクエストで指定する単位が完全に一致していないとデータは返ってこない
