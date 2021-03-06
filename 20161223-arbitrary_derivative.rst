==========================
有关任意阶导数的一个反例
==========================
:Author: Hau Wong
:Date:   2016-12-23
:Category: 分析

定义在区间 :math:`[-a,a]`\上的函数 :math:`f(x),(a>0)`\, 满足 :math:`\forall n\in\mathbb{N}_{+},f^{(n)}(0)=0`\，

问是否一定 :math:`\exists \delta>0,N>0`\,使当 :math:`n>N`\时， :math:`\forall x\in (-\delta,\delta)`\,都有 :math:`f^{(n)}(x)=0`\?

答：否。反例：

.. math::

   f(x)=
   \left\{
   \begin{array}{ll}
   e^{-x^{-2}},x\neq 0 \\ 0,x=0\\\end{array}
   \right.
