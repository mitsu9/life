# Nature Remo APIの使い方

Nature Remoを買ったのでAPIを使ってみる。

## Access tokenの取得

https://home.nature.global/
-> Generate access token

## 適当にリクエストを飛ばしてみる

/1/devicesにリクエストするとID, ファームウェアのバージョン、センサー情報などが返ってくる。

```
>>> curl -X GET "https://api.nature.global/1/devices" -H "accept: application/json" -k --header "Authorization: Bearer ACCESS_TOKEN"
[{"name":" Remo-mitsu9","id":"xxxxxxxxxxxxxxxxxxxxxxx","created_at":"2019-06-08T05:07:21Z","updated_at":"2019-06-09T15:29:34Z","mac_address":"xxxxxxxxxxxx","serial_number":"xxxxxxxxx","firmware_version":"Remo/1.0.77-g808448c","temperature_offset":0,"humidity_offset":0,"users":[{"id":"xxxxxxxxxxxxxxxxxxxxxxxx","nickname":"mitsu9","superuser":true}],"newest_events":{"hu":{"val":60,"created_at":"2019-06-09T17:24:37Z"},"il":{"val":245.8,"created_at":"2019-06-10T01:59:18Z"},"te":{"val":23.2,"created_at":"2019-06-09T22:08:07Z"}}}]%
```

## API Document

http://swagger.nature.global/

