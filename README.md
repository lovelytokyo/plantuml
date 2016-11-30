# 概要
plantumlの演習を目的としたレポジトリーです。

# 前提
- Mac
- Atomがインストールされていること
- javaがインストールされていること

# plantUMLインストール
[ココ](http://plantuml.com/download)からPlantUML compiled Jarをダウンロードする
ダウンロードしたファイル`plantuml.jar`は、PlantUMLファイルを画像化する時に使います。

# Atom pluginインストールと設定
## atom pluginインストール
- plantuml-viewer
- language-plantuml

## plantuml-viewer plugin設定
- `Charset`を`utf8`にすること
- 再起動（自分は再起動しないとViewが表示されませんでした）

# サンプルコード
```sample.pu
@startuml{you&i.png}
you -> I : hello
I -> you : hello
|||
loop 1, 3
  you -> I : shall we dance?
end
|||
you <- I : sure, my pleasure♡
note right: oh! handsome guy♪
@enduml

```
# ビューを表示する
`Control`+`option`+`p`でViewを表示する
<img width="1329" alt="スクリーンショット 2016-11-30 午後0.03.59.png" src="https://qiita-image-store.s3.amazonaws.com/0/34039/ef13a894-9d0a-45a8-9bbd-db4eed74c663.png">


# plantUMLファイルを画像化する

```
java -jar plantuml.jar file/sample.pu
```

`you&i.png`画像ファイルができる
