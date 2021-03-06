==========================
一次惊险的apt remove
==========================
:Author: Hau Wong
:Date:   2020-09-20
:Category: Linux

准备卸载alsa,由于包比较多，我就直接用通配符了：

.. code:: shell

   sudo apt remove alsa*

就在准备关掉终端时...我发现除了卸载了alsa之外，还卸载了三个不是alsa开头的包，分别是mint-meta-core,ubuntu-drivers common,mintdrivers

机智如我，赶快又把这三个包又装回去了。reboot后，没有异常，长舒一口气。。。

上网查了一下，被这样坑过的不止我一个。比如在Linux Mint社区的
`这里
<https://community.linuxmint.com/software/view/mint-meta-core>`_.

一位老哥坦言:

  “Essential package, don\'t uninstall it...”

寥寥一句话，语气中满是无奈啊！

以后用apt remove还是要小心一点。。。

