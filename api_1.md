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


### 個人データ取得 [GET]

+ Response 200 (application/json)

    + Body

        ```json
        {
          "user": {
            "id": 123456789,
            "name": "the40san",
            "avater_id": 1,
            "rank": 123,
            "exp": 12345678
          }
        }
        ```

### ユーザー設定変更 [PATCH]

+ Attributes

    + name: `` (string, optional) - ユーザー名
    + avater_id: `` (string, optional) - アバターID

+ Request example ユーザー名変更 (application/json)

    + Body

        ```js
        {
          "name": "つよい"
        }
        ```
+ Request example アバターID変更 (application/json)

    + Body

        ```js
        {
          "avater_id": 2
        }
        ```

+ Response 200 (application/json)

    + Body

        ```json
        {
          "user": {
            "id": 123456789,
            "name": "the40san",
            "avater_id": 1,
            "rank": 123,
            "exp": 12345678
          }
        }
        ```
