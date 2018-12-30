# 課題２レポート

原画像を白黒濃淡画像に変換し、2階調、4階調、8階調の画像を生成した。変換後の白黒濃淡画像を図１に示す。

![1](https://user-images.githubusercontent.com/46117925/50545423-b848a480-0c56-11e9-8338-2e19c8b43c50.PNG)  
図１　白黒濃淡画像

以下の手順を用いて白黒濃淡画像の階調を変化させた。

% ２階調画像の生成  
IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;

% ４階調画像の生成  
IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar;  axis image;

% ８階調画像の生成  
 IMG0 = ORG>32;  
 IMG1 = ORG>64;  
 IMG2 = ORG>96;  
 IMG3 = ORG>128;   
 IMG4 = ORG>160;  
 IMG5 = ORG>192;  
 IMG6 = ORG>224;  
 IMG = IMG0 + IMG1 +IMG2 + IMG3 + IMG4 + IMG5 + IMG6;  
 imagesc(IMG); colormap(gray); colorbar;  axis image;
 
生成した２階調、４階調、８階調の画像をそれぞれ図２，３，４に示す。

![2](https://user-images.githubusercontent.com/46117925/50545461-a0255500-0c57-11e9-85c8-2fdfda1ce91b.PNG)  
図２　２階調画像

![3](https://user-images.githubusercontent.com/46117925/50545462-a287af00-0c57-11e9-8ee7-8191b26bba8a.PNG)  
図３　４階調画像

![4](https://user-images.githubusercontent.com/46117925/50546229-88ee6380-0c67-11e9-8f61-6f35261bd39a.jpg)  
図４　８階調画像

以上の結果から階調が大きくなるほど鮮やかな画像になることが分かる。
