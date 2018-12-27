#課題３レポート

カラーな原画像を白黒濃淡画像に変換し、閾値処理を行なった。原画像の白黒濃淡画像を表示した結果を図１に示す。

![1](https://user-images.githubusercontent.com/46117925/50484255-d930b000-0a32-11e9-9aa6-20471eea07aa.PNG)

図１　白黒濃淡画像

以下のプログラムを用いて輝度値が一定以上の画素を白に、一定以下の画素を黒に変換した。xには輝度値の閾値が入る。

IMG = ORG > x; % 輝度値がx以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

閾値を64,96,128,192としたときの変換結果をそれぞれ図2~5に示す。

![2](https://user-images.githubusercontent.com/46117925/50484267-e64d9f00-0a32-11e9-85ff-3437b55bc500.PNG)

図２　輝度値の閾値を64にしたときの変換画像

![3](https://user-images.githubusercontent.com/46117925/50484279-f2d1f780-0a32-11e9-96d1-988b4824f349.PNG)

図３　輝度値の閾値を96にしたときの変換画像

![4](https://user-images.githubusercontent.com/46117925/50484291-fc5b5f80-0a32-11e9-84dc-a3f864452c18.PNG)

図４　輝度値の閾値を128にしたときの変換画像

![5](https://user-images.githubusercontent.com/46117925/50484299-0ed59900-0a33-11e9-9062-d084dc20fb29.PNG)

図５　輝度値の閾値を192にしたときの変換画像


以上の結果から、白黒画像の輝度値は値が大きいほど白に近く閾値が大きくなるほど黒色の画素が多くなっている事が分かる。
