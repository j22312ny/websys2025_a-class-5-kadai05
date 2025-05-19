## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
・エンドポイント：https://zipcloud.ibsnet.co.jp/api/search
・機能：郵便番号から日本国内の都道府県・市区町村・町域を検索し、住所を返す無料のAPI。
* リクエストとレスポンスのフォーマット

### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
* エンドポイントと機能
1.位置検索API
　・エンドポイント：https://geocoding-api.open-meteo.com/v1/search
　・機能：都市名を指定すると緯度・経度を取得できる。
2.天気予報API
　・エンドポイント：https://api.open-meteo.com/v1/forecast
　・機能：緯度・経度を使って現在の気温、風速、天気コードなどを取得できる。
* リクエストとレスポンスのフォーマット
・位置検索API
https://geocoding-api.open-meteo.com/v1/search?name=Tokyo&count=1&language=ja
　・レスポンス
{
  "results": [
    {
      "name": "Tokyo",
      "latitude": 35.6828,
      "longitude": 139.759
    }
  ]
}
・天気予報API
https://api.open-meteo.com/v1/forecast?latitude=35.6828&longitude=139.759&current_weather=true
　・レスポンス
{
  "current_weather": {
    "temperature": 18.5,
    "windspeed": 5.1,
    "weathercode": 1
  }
}
### Q3-3. 感想
* 今回の課題で苦労したこと
都市名から緯度・経度を取得するために別のAPI（ジオコーディング）を使う必要があり、その関係を理解するのに時間がかかった。
* 演習を通して理解できたこと
Web APIの呼び出しや、どのように画面に表示させるかを実際に体験することで、API連携の流れを理解することができた。
* Web APIの利便性や課題など
Web APIを使うことで、外部のデータを簡単に取得することができるため、アプリの機能を大きく広げることができる。
