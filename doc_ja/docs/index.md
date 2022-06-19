# MocapForStreamerって何？

<iframe width="560" height="315" src="https://www.youtube.com/embed/PeQOcDB1x8A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

二つのウェブカメラをステレオカメラとして用いて、上半身の簡易なモーションキャプチャを行うWindowsアプリケーションです。

## 特徴

下記のものがあれば、特別な装置を必要とすることなく、人の上半身の動きをリアルタイムでをキャプチャすることができます。

- ミドルクラスのPC
- 2台の同一機種のウェブカメラ

また、キャプチャした動きは、VMCプロトコルで出力することができます。

## [MocapForAll](https://akiya-research-institute.github.io/MocapForAll-Manual/)というのもあるみたいだけど、何がちがうの？

MocapForStreamerは、上半身のキャプチャのみに機能を絞り、カメラに制約を課すことで、カメラキャリブレーション等のセットアップを大きく簡略化しています。

| 機能 | MocapForStreamer | MocapForAll |
| ------- | ---------------- | ----------- |
| 上半身のキャプチャ |Yes|Yes|
| 下半身のキャプチャ |No|Yes|
| 使用できるカメラの数|必ず2個|2個以上、上限なし|
| カメラ配置の制約|必ず並行に配置|制約なし|
| カメラ機種の制約|必ず同一機種|同一機種である必要なし|
