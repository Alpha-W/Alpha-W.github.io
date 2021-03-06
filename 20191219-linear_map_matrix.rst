==========================
线性映射与矩阵
==========================
:Author: Hau Wong
:Date:   2019-12-19
:Category: 代数

线性映射的矩阵表示
==========================
设 :math:`V_1,V_2`\分别为域 :math:`F`\上的 :math:`n`\维与 :math:`m`\维线性空间， :math:`\phi\in Hom(V_1,V_2)`\.又设矩阵 :math:`A`\为域 :math:`F`\上的 :math:`m\times n`\阶矩阵，即 :math:`A\in M_{m\times n}(F)`\.定义 :math:`\mathcal{A}:F_n\to F_m,x\mapsto Ax`\故 :math:`\mathcal{A}\in Hom(F^n,F^m)`\.由于 :math:`Hom(F^n,F^m)\cong Hom(V_1,V_2)`\.我们想到能否用 :math:`\mathcal{A}`\来表示 :math:`\phi`\.即能否将一般的线性映射归结为“用矩阵左乘”这样的线性映射?下面证明之.

取定 :math:`V_1,V_2`\的一组(有序)基 :math:`\alpha_1,...,\alpha_n`\与 :math:`\beta_1,...,\beta_m`\.

设 :math:`\phi \alpha_j=\sum_{k=1}^m a_{kj}\beta_k=(\beta_1,...,\beta_m)(a_{1j},...,a_{mj})^T`\  :math:`(j=1,2,...,n)`\  :math:`\phi(\alpha_1,...,\alpha_n)=(\phi\alpha_1,...,\phi\alpha_n)=(\beta_1,...,\beta_m)A`\.

:math:`\forall\alpha=(\alpha_1,...,\alpha_n)(x_1,...,x_n)^T,(x_1,...,x_n)^T`\为 :math:`\alpha`\在基 :math:`\alpha_1,...,\alpha_n`\下的坐标.

:math:`\phi\alpha=(\phi\alpha_1,...,\phi\alpha_n)(x_1,...,x_n)^T=\phi(\alpha_1,...,\alpha_n)(x_1,...,x_n)^T=(\beta_1,...,\beta_m)A(x_1,...,x_n)^T`\

即 :math:`\phi\alpha`\在基 :math:`\beta_1,...,\beta_m`\下的坐标为 :math:`A(x_1,...,x_n)^T`\

记 :math:`C_1((\alpha_1,...,\alpha_n)(x_1,...,x_n)^T)=(x_1,...,x_n)^T,C_2((\beta_1,...,\beta_m)(x_1,...,x_m)^T)=(x_1,...,x_m)^T`\

则有交换图:

.. math::

   \require{AMScd}\begin{CD}V_1@>{\phi}>>V_2\\@V{C_1}VV@V{C_2}VV\\F^n@>{\mathcal{A}}>>F^m\end{CD}

故有以下定理：

设 :math:`\phi\in Hom(V_1,V_2),dimV_1=n,dimV_2=m`\.于 :math:`V_1.V_2`\中分别取定一组(有序)基 :math:`\alpha_1,...,\alpha_n`\与 :math:`\beta_1,...,\beta_m`\后,以 :math:`\phi\alpha_1,...,\phi\alpha_n`\的坐标列作矩阵 :math:`A`\,即 :math:`\phi(\alpha_1,...,\alpha_n)=(\beta_1,...,\beta_m)A`\.则 :math:`\forall\alpha\in V_1,\beta=A\alpha\Leftrightarrow y=Ax`\.其中 :math:`x,y`\分别为 :math:`\alpha,\beta`\的坐标列. :math:`A`\称为 :math:`\phi`\的矩阵表示.

矩阵的四个空间
==========================
设 :math:`\mathcal{A}:F_n\to F_m,x\mapsto Ax`\的伴随为 :math:`\mathcal{A}^\star:F_n\to F_m,x\mapsto Ax`\.则有:

:math:`A`\的右零空间 :math:`=ker\mathcal{A}=\{x\mid Ax=0\}=\{x^T\mid x^TA^T=0\}=ker\mathcal{A}^\star=A^T`\的左零空间.

:math:`A`\的列空间 :math:`=Im\mathcal{A}=<\alpha_1,...,\alpha_n>=<(\alpha_1^T)^T,...,(\alpha_n^T)^T>=Im\mathcal{A}^\star=A^T`\的左零空间.

:math:`ker\mathcal{A}\oplus Im\mathcal{A}^\star=F^n`\

:math:`ker\mathcal{A}^\star\oplus Im\mathcal{A}=F^m`\

矩阵的逆，左逆，右逆
==========================
:math:`A`\列满秩 :math:`\Leftrightarrow A`\有左逆 :math:`\Leftrightarrow\mathcal{A}`\是单射, :math:`\mathcal{A}^\star`\是满射 :math:`\Leftrightarrow`\  :math:`dimker\mathcal{A}=0,dimker\mathcal{A}^\star=m-n.dimIm\mathcal{A}=dimIm\mathcal{A}^\star=n`\.

:math:`A`\行满秩 :math:`\Leftrightarrow A`\有右逆 :math:`\Leftrightarrow\mathcal{A}`\是满射, :math:`\mathcal{A}^\star`\是单射 :math:`\Leftrightarrow`\  :math:`dimker\mathcal{A}=n-m,dimker\mathcal{A}^\star=0.dimIm\mathcal{A}=dimIm\mathcal{A}^\star=m`\.

:math:`A`\可逆 :math:`\Leftrightarrow A`\有左逆且 :math:`A`\有右逆.
