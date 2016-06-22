#Three.js
######Three.js是一个3D JavaScript库
Three.js封装了底层的图形接口，使程序员能够在无需掌握繁冗的图形学知识的情况下，也能用简单的代码实现三维场景的渲染。它实现了更高程度的封装，同时保证了灵活性。Three.js提供了基于WebGL、Canvas、SVG标签的渲染，但由于通常WebGL能够实现更灵活的渲染效果，我们这里使用基于WebGL渲染器的实现。

######使用协议
Three.js是基于MIT协议进行发布的，因此使用和发布都非常自由。

######第一章 Hello, World
* chpt-1-1-helloWorld.html  
练习了如何引用Three.js, 以及渲染器（Renderer)、场景(Scene)、照相机(Camera)的创建和使用，以及如何创建一个长方体。

######第二章 照相机（Camera)
* chpt-2-1-Orchographic-camera.html
* chpt-2-2-Perspective-Camera.html 

照相机定义了三维空间到二维屏幕的投影方式，从而实现了三维的场景显示到二维的显示屏上。针对投影方式的不同，照相机分为正交投影照相机和透视投影照相机。

二者之间的区别在于：使用正交投影照相机获得的结果就像我们在数学几何学课上老师教我们画的，对于在三维空间内平行的线，投影到二维空间中也一定是平行的,如下图(b)而透视投影照相机获得的结果是类似人眼在真是世界中看到的“近大远小”的效果,如下图(a)。

![image](https://github.com/ChengYiFan/three.js/raw/master/img/camera.jpg)

######第三章 几何形状
在创建物体时，需要传入两个参数，一个是几何形状(Geometry)，另一个是材质(Material)。几何形状(Geometry)最主要的功能是储存了一个物体的顶点信息。

WebGL需要程序员指定每个顶点的位置，而在Three.js中，可以通过指定一些特征来创建几何形状，例如使用半径创建一个球体，从而省去程序员一个个指定顶点的工作量。

* chpt-3-1-Geometry.html   如图chpt-3-1 练习立方体、平面、球体
* chpt-3-2-Geometry.html   如图chpt-3-2 练习圆形、圆柱体、正十二面体
* chpt-3-3-Geometry.html   如图chpt-3-3 练习圆环面、圆环结  
* chpt-3-4-Geometry.html   如图chpt-3-4 练习自定义形状。

图chpt-3-1
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry.png)

图chpt-3-2
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry2.png)

图chpt-3-3
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry3.png)

图chpt-3-4
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry4.png)

######第四章 材质
材质（Material）是独立于物体顶点信息之外的与渲染效果相关的属性。通过设置材质可以改变物体的颜色、纹理贴图、光照模式等。

本章将介绍基本材质、两种基于光照模型的材质，以及使用法向量作为材质。除此之外，本章还将介绍如何使用图像作为材质。

* chpt-4-1-Material.html             练习基本材质
* chpt-4-2-MeshLambertMaterial.html  练习Lambert材质
* chpt-4-3-MeshPhongMaterial.html    练习Phong材质
* chpt-4-4-MeshNormalMaterial.html   练习法向材质




######第八章 光与影
图片渲染的丰富效果很大程度上也要归功于光与影的利用。为了使计算机模拟丰富的光照效果，人们提出了几种不同的光源模型（环境光、平行光、点光源、聚光灯等），在不同场合下组合利用，将能达到很好的光照效果。

在Three.js中，光源与阴影的创建和使用是十分方便的。在学会了如何控制光影的基本方法之后，如果能将其灵活应用，将能使场景的渲染效果更加丰富逼真。在本章中，我们将探讨四种常用的光源（环境光、点光源、平行光、聚光灯）和阴影带来的效果，以及如何去创建使用光影。

环境光是指场景整体的光照效果，是由于场景内若干光源的多次反射形成的亮度一致的效果，通常用来为整个场景指定一个基础亮度。因此，环境光没有明确的光源位置，在各处形成的亮度也是一致的。

在设置环境光时，只需要指定光的颜色：THREE.AmbientLight(hex)
