# 課題７レポート

原画像を白黒濃淡画像に変換し、ダイナミックレンジを変化させ濃度ヒストグラムを見た。原画像の白黒濃淡画像を図１に示す。

![1](https://user-images.githubusercontent.com/46117925/50546505-09af5e80-0c6c-11e9-90fc-adddd0d19127.PNG)  
図１　白黒濃淡画像

以下の手順を用いて図１の濃度ヒストグラムを表示した。結果を図２に示す。

imhist(ORG);

![2](https://user-images.githubusercontent.com/46117925/50546506-0ddb7c00-0c6c-11e9-9e3e-ee40a008f7a4.PNG)  
図２　図１の濃度ヒストグラム

また、以下の手順を用いてダイナミックレンジを255に変更し濃度ヒストグラムを表示した。

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
ORG = uint8(ORG);  
imhist(ORG); % 濃度ヒストグラムを生成、表示

ダイナミックレンジを変更した画像を図３に、ダイナミックレンジ変更後の濃度ヒストグラムを図４に示す。

![3](https://user-images.githubusercontent.com/46117925/50546508-10d66c80-0c6c-11e9-89ec-d6b8ee6ec5c0.PNG)  
図３　ダイナミックレンジ255の白黒濃淡画像

![4](https://user-images.githubusercontent.com/46117925/50546510-12a03000-0c6c-11e9-8048-78ff37cadd0e.PNG)  
図４　ダイナミックレンジ変更後の濃度ヒストグラム

また、上記の「ORG = uint8(ORG);」では画像を符号無し８ビット整数配列に変更している。
