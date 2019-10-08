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


+ Response 200 (application/json)

パスの具体的な中身はまだ未定。
pngなのかも未定。

    + Body
    
        ```json
        {
          "total": 43,
          "urls_s3": [
            "s3://bellface-sdp-infra-dev/sceen-pickup/{meeting_id}-{second}.png",
            "s3://bellface-sdp-infra-dev/sceen-pickup/{meeting_id}-{second}.png",
            "s3://bellface-sdp-infra-dev/sceen-pickup/{meeting_id}-{second}.png",
            "s3://bellface-sdp-infra-dev/sceen-pickup/{meeting_id}-{second}.png",
          ]
        }
        ```

