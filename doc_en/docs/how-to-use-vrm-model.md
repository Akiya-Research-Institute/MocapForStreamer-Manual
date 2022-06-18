# VRMモデルの読み込み

## ファイルの読み込み

VRMファイルをMocapForStreamerのウィンドウにドラッグ＆ドロップすることで、モデルを読み込むことができます。

## 目のボーンの設定

モデルによって目のボーンの名前が異なります。自動でボーンを検出できなかった場合は、瞳が動きません。  
その際は、画面左の「Facial expression settings」を開き、「Eye bone override」の下で目のボーンの名前を手動で指定してください。  
また、瞳の動きの範囲が適切でない場合は、「Max angle」を調整してください。

## 顔のMorph target (Blend shape)の設定

モデルによってMorph Targetの名前が異なります。デフォルトでは、[パーフェクトシンク](https://hinzka.hatenablog.com/entry/2020/08/15/145040)で使われる名前のMorph Targetがある前提としています。  
モデルがそれ以外の名前でMorph Targetを持っている場合は、画面左の「Facial expression settings」を開き、適切なMorph Target名を手動で入力してください。  
なお、VRoid Studioで作成したモデルに対してMorph Targetを適当に設定した状態のプリセットがあります。「Load preset...」から、VRoidのβ版または最新版のプリセットを読み込んでください。