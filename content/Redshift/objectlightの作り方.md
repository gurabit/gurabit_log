---
title: "メッシュライトの作り方"
date: 2021-06-18T14:47:04+09:00
draft: true
---

## HoudiniのRedshiftでメッシュライトを作る方法。
よくRedshiftでメッシュライトってどうやって作るんだっけ？となるのでメモ。（今までオブジェクトライトという名称だと思ってたけど、メッシュライトという言い方が正しいっぽい）。



#### LightとObjectを作る
![](https://raw.githubusercontent.com/gurabit/gurabit_log/master/images/Redshift/Mesh_Light/objectlight_img%20(3).png)

まずメッシュライトにしたいオブジェクトとRSLightを作る。


#### Light TypeをAreaにする
![](https://raw.githubusercontent.com/gurabit/gurabit_log/master/images/Redshift/Mesh_Light/objectlight_img%20(4).png)

RSLightのLightタブを選択。

Light TypeのAreaを選択。


#### ShapeをMeshにする
![](https://raw.githubusercontent.com/gurabit/gurabit_log/master/images/Redshift/Mesh_Light/objectlight_img%20(6).png)

スクロールしてAreaのところのShapeのMeshを選択。


#### Mesh LightにしたいObjectノードを選択
![](https://raw.githubusercontent.com/gurabit/gurabit_log/master/images/Redshift/Mesh_Light/objectlight_img%20(7).png)

Mesh Objectの右端の矢印キーみたいなやつを選択。


![](https://raw.githubusercontent.com/gurabit/gurabit_log/master/images/Redshift/Mesh_Light/objectlight_img%20(8).png)

ノード選択のウィンドウが出るのでメッシュライトにしたいノードを選択。


![](https://raw.githubusercontent.com/gurabit/gurabit_log/master/images/Redshift/Mesh_Light/objectlight_img%20(9).png)

オブジェクトがメッシュライトに！