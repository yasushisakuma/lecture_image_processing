# 課題１レポート

図1に示す画像を原画像とする．この画像はフリー画像サイト「Pixabay」から引用した画像である.

原画像を読み込み，表示した結果を図１に示す．
![default](https://user-images.githubusercontent.com/46117925/50482312-46d7de80-0a29-11e9-8d45-e4ebb0b53d80.PNG)  
図1 原画像

原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．なお，拡大する際には，単純補間するために「box」オプションを設定する．

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

1/2サンプリングの結果を図２に示す．

![default](https://user-images.githubusercontent.com/46117925/50482136-71756780-0a28-11e9-8082-0230b69875ac.PNG)  
図2 1/2サンプリング

1/4から1/32サンプリングは上記の操作を繰り返す事で得られる．サンプリングの結果を図３～６に示す．

![3](https://user-images.githubusercontent.com/46117925/50482476-193f6500-0a2a-11e9-92d4-cdf0b27a4d29.PNG)  
図3 1/4サンプリング

![4](https://user-images.githubusercontent.com/46117925/50482500-3d9b4180-0a2a-11e9-97e9-6408b32e0966.PNG)

図4 1/8サンプリング

![5](https://user-images.githubusercontent.com/46117925/50482523-59064c80-0a2a-11e9-958e-4cc5b8807efe.PNG) 

図5 1/16サンプリング

![6](https://user-images.githubusercontent.com/46117925/50482546-6f140d00-0a2a-11e9-988b-1eff6192d179.PNG)

図6 1/32サンプリング

このようにサンプリング幅が大きくなると，モザイク状のサンプリング歪みが発生し大きくなっていく事が分かる．
