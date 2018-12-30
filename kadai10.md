# 課題10レポート

原画像を白黒濃淡画像に変換し、エッジ抽出を行った。変換後の白黒濃淡画像を図１に示す。

![1](https://user-images.githubusercontent.com/46117925/50545073-453a3080-0c4c-11e9-85e3-b537a26befa4.PNG)  
図１　白黒濃淡画像

今回はプレウィット法・ソベル法・キャニー法の3つの方法を用いてエッジ抽出を行った。エッジ抽出の手順は以下の通りである。

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  
IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  

エッジ抽出の結果を図２，３，４に示す。

![2](https://user-images.githubusercontent.com/46117925/50545075-479c8a80-0c4c-11e9-9584-8edd172be0c7.PNG)  
図２　プレウィット法によるエッジ抽出

![3](https://user-images.githubusercontent.com/46117925/50545076-49664e00-0c4c-11e9-94d2-65fab99f15d7.PNG)  
図３　ソベル法によるエッジ抽出

![4](https://user-images.githubusercontent.com/46117925/50545077-4bc8a800-0c4c-11e9-979d-0317c4546d43.PNG)  
図４　キャニー法によるエッジ抽出

以上の結果から、今回はプレウィット法とソベル法では抽出したエッジに大きな違いは見られなかったが、キャニー法は他の方法よりも多くのエッジを抽出している事が分かる。
