# 課題８レポート

原画像を白黒濃淡画像に変換し、閾値で二値化された画像の連結成分にラベルを付けた。変換後の白黒濃淡画像を図１に示す。

![1](https://user-images.githubusercontent.com/46117925/50546671-ee921e00-0c6e-11e9-86fa-6cb00f998fd8.PNG)  
図１　白黒濃淡画像

以下の手順を用いて白黒濃淡画像を閾値128で二値化し、連結成分のラベル付けを行った。それぞれの結果を図２，３に示す。

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  
IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示  
pause;  

![2](https://user-images.githubusercontent.com/46117925/50546672-f05be180-0c6e-11e9-91a7-ec006c2ae399.PNG)  
図２　閾値128で二値化した白黒濃淡画像

![3](https://user-images.githubusercontent.com/46117925/50546673-f225a500-0c6e-11e9-8102-04d7acd5fa78.PNG)  
図３　連結成分のラベル付け
