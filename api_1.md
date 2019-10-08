# Scene Pick-up API
場面ピックアップ用のAPI


## 場面ピックアップAPI [POST /pickup]

+ Request (application/json)

    + Attribute
        + meeting_id: 981451 (number) - 商談id
        + seconds: 124 (number) - 時間(秒)
        + staff_ids: 65141,12515,153235 (string) - スタッフidの列。カンマ区切り
        + date_from: 2019-10-01 (string) - 検索範囲日 開始
        + data_to: 2019-10-10 (string) - 検索範囲日 終了
        + max_res: 100 (number) - 最大レスポンス数


+ Response 200 (application/json)

パスの具体的な中身はまだ未定。
pngなのかも未定。

    + Body
    
        ```json
        {
          "total": 4,
          "res": [
            {
                "meeting_id": 65114,
                "second": 123, 
                "image_url": "s3://bellface-sdp-infra-dev/sceen-pickup/{meeting_id}-{second}.png",
                "staff_name": "ベル 太郎",
                "datetime": "2019-10-10T14:23:12",
                "customer_company": "ABC株式会社",
                "customer_name": "部長",
                "customer_position": "田中 一郎",               
            }, 
            {
                "meeting_id": 765444,
                "second": 153, 
                "image_url": "s3://bellface-sdp-infra-dev/sceen-pickup/{meeting_id}-{second}.png",
                "staff_name": "フェイス 次郎",
                "datetime": "2019-10-11T15:33:16",
                "customer_company": "DEF株式会社",
                "customer_name": "次長",
                "customer_position": "佐藤 五郎",               
            }, 
          
          ]
        }
        ```

