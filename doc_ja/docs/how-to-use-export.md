# 出力設定

## 背景色の変更

クロマキー合成等のために背景色を変更するには、画面左の「Environment settings」メニューから「Background color」を変更してください。

## モーションデータ出力

BVH形式のファイルへ保存、または、VMCプロトコルでリアルタイムに他のアプリケーションにデータを送信できます。

### BVHファイルへ保存

画面左の「Export settings」メニューから「Start BVH recording」をクリックし、保存先を選択してください。  
再度同じボタンを押すか、画面右上に表示される停止ボタンを押すと、BVHファイルが出力されます。

### VMCプロトコル出力

画面左の「Export settings」メニューから「Send VMC protocol」を有効化してください。  

!!! Info "VMCプロトコルの簡単な説明"
    VMCプロトコルは、キャラクターのボーンや表情モーフ等の情報をアプリケーション間でリアルタイムに送受信するためのメッセージのフォーマットです。  
    プロトコルの詳細は、[https://protocol.vmc.info/](https://protocol.vmc.info/) をご覧ください。

    なお、VMCプロトコルでのデータ送受信には、[Virtual Motion Capture](https://vmc.info/) のアプリケーション自体は必要ではないことに注意してください。

## 動画ストリーム出力

SpoutまたはNDI®により、MocapForStreamerの画面をリアルタイムに他のアプリケーションへ送信することができます。

送信される画面は、透明度(アルファチャンネル)を含みます。  
画面左の「Environment settings」メニューから「Background color」の「A」をゼロにすることで、背景を透過した画面を送信することができます。

下記は両者の簡単な比較です。

| 特徴 | Spout | NDI |
| ------- | ---------------- | ----------- |
| アプリ間の送信 |✅|✅|
| PC間の送信 |✖|✅|
| フレームレート | 高 | 低 |
| 遅延 | 数フレーム程度 | ネットワークに依存 |

### Spout出力

画面左の「Export settings」メニューから「Send Spout video stream」を有効化してください。  
「MocapForStreamer」という名前で送信が開始されます。

!!! Info "Spoutとは"
    GPUの共有メモリを介してアプリケーション間でリアルタイムに動画像を共有する仕組みです。  
    詳細および各種ツールは[こちら](https://spout.zeal.co/)をご覧ください。

!!! Info "Spout2 Plugin for OBS Studio"
    [OBSでSpout2の画像を送受信するためのプラグイン](https://github.com/Off-World-Live/obs-spout2-plugin)が公開されています。

### NDI出力

画面左の「Export settings」メニューから「Send NDI video stream」を有効化してください。  
「MocapForStreamer」という名前で送信が開始されます。

NDIを使うと、MocapForStreamerの画面をリアルタイムにローカルネットワーク内の他のデバイスに送信することができます。  
例えば、MocapForStreamerによるモーションキャプチャを行うPCと、その画面を他の素材等と合成して動画配信を行うPCを分けるといった利用が可能です。

!!! Info "NDI® is a registered trademark of NewTek, Inc."
    See [http://ndi.tv/](http://ndi.tv/) for the details.  
    You can download "NDI Tools" software suites for various platforms directly from this site. [http://ndi.tv/tools/](http://ndi.tv/tools/)

!!! Info "OBS-NDIプラグイン"
    NDIで送信された画面を[OBSで受信するためのプラグイン](https://obsproject.com/forum/resources/obs-ndi-newtek-ndi%E2%84%A2-integration-into-obs-studio.528/)が公開されています。

!!! Failure "他のデバイスにうまく送信できない場合"
    ファイアウォールにより通信が阻害されている可能性があります。  
    ファイアウォールを無効化するか、NDIが使用するポートでの通信を許可してみてください。  
    NDIが使用するポートは、[こちら](https://support.newtek.com/hc/en-us/articles/218109497-NDI-Video-Data-Flow)に記載の通り**49152**から**65535**です。