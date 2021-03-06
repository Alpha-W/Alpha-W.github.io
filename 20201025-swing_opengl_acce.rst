============================
Swing启用硬件加速
============================
:Author: Hau Wong
:Date:   2020-10-25
:Category: Java

刷知乎无意中看到
`这个帖子，
<https://www.zhihu.com/question/323058868/answer/811401387>`_,
才知道swing还可以开硬件加速。在此之前每次打开idea都要等很长一段时间，开了硬件加速之后打开速度就快了许多。

方法：

找到idea的安装目录(比如我的安装目录是/home/hau/idea/)，在安装目录下的./bin文件夹内找到idea.vmoptions和idea64.vmoptions两个文件，分别在这两个文件末尾追加新的一行：

.. code::

   -Dsun.java2d.opengl=true

然后保存退出，再打开idea时就会比之前快很多。

以上方法也适用于jetbrains的其他IDE。

