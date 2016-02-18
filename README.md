# Net Radio Archive modified version

## What's this?

* 本家 Net Radio Archive <https://github.com/yayugu/net-radio-archive> の個人的フォーク版です。

## What's the difference?

* らじるらじる対応 (2016/02/05 に本家に取り込まれました)

settings.yml の radiru_channels で、録音したいチャンネルを指定してください。
(r1: ラジオ第1、r2: ラジオ第2、fm: NHK-FM)

今のところ録音できるのは、東京からの放送のみです。地方放送の番組情報を
取得する API がわかれば対応できるのですが。

* 超A&G、Radiko、らじるらじるの録音タスクのマルチスレッド化

本家では録音タスク起動の仕様上、同一時刻に始まる番組が多く重なると、
録音開始が遅れる / 録音できなくなるという制限があります。
(番組開始前に録音が始められるのは 5つまで / 同時録音数は 7つまで)

ここのフォーク版では、番組開始前にいっぺんに必要数の録音タスクを
マルチスレッドで起動するため、上記制限がありません。

## License

* 本家と同じ MIT License とします。

