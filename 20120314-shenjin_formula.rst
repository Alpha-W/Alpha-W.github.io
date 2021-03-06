==========================
盛金公式与盛金定理
==========================
:Author: Hau Wong
:Date:   2012-03-14
:Category: 代数

在一元三次方程

:math:`ax^3+bx^2+cx+d=0`\ , :math:`(a,b,c,d\in\mathbb{R},a\neq 0)`\中：

重根判别式： :math:`A=b^2-3ac,B=bc-9ad,C=c^2-3bd`\

总判别式： :math:`\Delta=B^2-4AC`\

1.当 :math:`A=B=0`\时， :math:`x_{1}=x_{2}=x_{3}=-\frac{b}{3a}=-\frac{c}{b}=-\frac{3d}{c}`\

2.当 :math:`\Delta=0`\时， :math:`x_{1}=-\frac{b}{a}+K,x_{2}=x_{3}=-\frac{K}{2}`\

​(其中 :math:`K=\frac{B}{A},A\neq 0`\)

3.当 :math:`\Delta>0`\时，

:math:`x_{1}=\frac{-b-\sqrt[3]{Y_{1}}-\sqrt[3]{Y_{2}}}{3a}\quad`\ :math:`x_{2,3}=\frac{-2b+\sqrt[3]{Y_{1}}+\sqrt[3]{Y_{2}}}{6a}\pm\frac{\sqrt{3}(\sqrt[3]{Y_{1}}-\sqrt[3]{Y_{2}})}{6a}i`\

(其中， :math:`Y_{1,2}=Ab+\frac{3a(-B\pm\sqrt{\Delta})}{2}`\)

4.当 :math:`\Delta<0`\时，

:math:`x_{1}=\frac{-b-2\sqrt{A}\cos(\frac{\theta}{3})}{3a}\quad`\  :math:`x_{2,3}=\frac{-b+\sqrt{A}(\cos(\frac{\theta}{3})\pm\sin(\frac{\theta}{3}))}{3a}`\

(其中， :math:`\theta=\arccos T,T=\frac{2Ab-3aB}{2\sqrt{A^3}}`\, :math:`A>0,-1<T<1`\)

盛金判别法：

1.当 :math:`\Delta>0`\时,方程有一个实根和一个共轭虚根.

2.当 :math:`\Delta=0`\时,方程有三个实根,其中有一个两重根.

3.当 :math:`\Delta<0`\时,方程有三个不相等的实根.

4.当 :math:`A=B=0`\时,方程有一个三重实根.

盛金定理：

定理1：当 :math:`A=B=0`\时，若 :math:`b=0`\,则 :math:`c=d=0`\.(此时方程有一个三重实根0)

定理2：当 :math:`A=B=0`\时，若 :math:`b\neq 0`\,则 :math:`c\neq 0`\.

定理3：当 :math:`A=B=0`\时, :math:`C=0`\

定理4：当 :math:`A=0`\时,若 :math:`B\neq 0`\,则 :math:`\Delta>0`\

定理5：当 :math:`A<0`\时， :math:`\Delta>0`\

定理6：当 :math:`\Delta=0`\时，若 :math:`B=0`\,则 :math:`A=0`\.

定理7：当 :math:`\Delta=0`\时，若 :math:`B\neq 0`\,则盛金公式2一定不存在 :math:`A\leq 0`\的值.

定理8：当 :math:`\Delta<0`\,盛金公式3一定不存在 :math:`A\leq 0`\的值.

定理9：当 :math:`\Delta<0`\,盛金公式3一定不存在 :math:`T\geq-1`\或 :math:`T\leq 1`\的值.

