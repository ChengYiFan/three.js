#Three.js
######Three.js是一个3D JavaScript库
Three.js封装了底层的图形接口，使程序员能够在无需掌握繁冗的图形学知识的情况下，也能用简单的代码实现三维场景的渲染。它实现了更高程度的封装，同时保证了灵活性。Three.js提供了基于WebGL、Canvas、SVG标签的渲染，但由于通常WebGL能够实现更灵活的渲染效果，我们这里使用基于WebGL渲染器的实现。

######使用协议
Three.js是基于MIT协议进行发布的，因此使用和发布都非常自由。

######Hello, World
* chpt-1-1-helloWorld.html  
练习了如何引用Three.js, 以及渲染器（Renderer)、场景(Scene)、照相机(Camera)的创建和使用，以及如何创建一个长方体。

######照相机（Camera)
* chpt-2-1-Orchographic-camera.html
* chpt-2-2-Perspective-Camera.html 

照相机定义了三维空间到二维屏幕的投影方式，从而实现了三维的场景显示到二维的显示屏上。针对投影方式的不同，照相机分为正交投影照相机和透视投影照相机。

二者之间的区别在于：使用正交投影照相机获得的结果就像我们在数学几何学课上老师教我们画的，对于在三维空间内平行的线，投影到二维空间中也一定是平行的,如下图(b)而透视投影照相机获得的结果是类似人眼在真是世界中看到的“近大远小”的效果,如下图(a)。
![image](https://github.com/ChengYiFan/three.js/raw/master/img/camera.jpg)

######几何形状
在创建物体时，需要传入两个参数，一个是几何形状(Geometry)，另一个是材质(Material)。几何形状(Geometry)最主要的功能是储存了一个物体的顶点信息。

WebGL需要程序员指定每个顶点的位置，而在Three.js中，可以通过指定一些特征来创建几何形状，例如使用半径创建一个球体，从而省去程序员一个个指定顶点的工作量。

* chpt-3-1-Geometry.html   练习立方体、平面、球体
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry.png)

* chpt-3-2-Geometry.html   练习圆形、圆柱体、正十二面体
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry2.png)

* chpt-3-3-Geometry.html   练习圆环面、圆环结
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry3.png)

* chpt-3-4-Geometry.html  练习自定义形状。
![image](https://github.com/ChengYiFan/three.js/raw/master/img/geometry4.png)