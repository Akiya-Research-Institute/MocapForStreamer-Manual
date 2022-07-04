# 出力設定

## 背景色の変更

クロマキー合成等のために背景色を変更するには、画面左の「Environment settings」メニューから「Background color」を変更してください。

## VMCプロトコル出力

画面左の「Export settings」メニューから「Send VMC protocol」を有効化してください。  

!!! Info "VMCプロトコルの簡単な説明"
    VMCプロトコルは、キャラクターのボーンや表情モーフ等の情報をアプリケーション間でリアルタイムに送受信するためのメッセージのフォーマットです。  
    プロトコルの詳細は、[https://protocol.vmc.info/](https://protocol.vmc.info/) をご覧ください。

    なお、VMCプロトコルでのデータ送受信には、[Virtual Motion Capture](https://vmc.info/) のアプリケーション自体は必要ではないことに注意してください。

## NDI®による動画ストリーム出力

画面左の「Export settings」メニューから「Send NDI」を有効化してください。  
「MocapForStreamer」という名前で送信が開始されます。

!!! Info "NDI® is a registered trademark of NewTek, Inc."
    See [http://ndi.tv/](http://ndi.tv/) for the details.  
    You can download "NDI Tools" software suites for various platforms directly from this site. [http://ndi.tv/tools/](http://ndi.tv/tools/)

!!! Info "OBS-NDIプラグイン"
    NDIで送信された画面を[OBSで受信するためのプラグイン](https://obsproject.com/forum/resources/obs-ndi-newtek-ndi%E2%84%A2-integration-into-obs-studio.528/)が公開されています。

### NDI出力でできること

NDIを使うと、MocapForStreamerの画面をリアルタイムにローカルネットワーク内の他のデバイスに送信することができます。  
例えば、MocapForStreamerによるモーションキャプチャを行うPCと、その画面を他の素材等と合成して動画配信を行うPCを分けるといった利用が可能です。

!!! Failure "他のデバイスにうまく送信できない場合"
    ファイアウォールにより通信が阻害されている可能性があります。  
    ファイアウォールを無効化するか、NDIが使用するポートでの通信を許可してみてください。  
    NDIが使用するポートは、[こちら](https://support.newtek.com/hc/en-us/articles/218109497-NDI-Video-Data-Flow)に記載の通り**49152**から**65535**です。

### 背景を透過した画像の出力

MocapForStreamerからNDIで送信される画面は、透明度(アルファチャンネル)を含んでいます。  
画面左の「Environment settings」メニューから「Background color」の「A」をゼロにすることで、背景を透過した画面を出力することができます。