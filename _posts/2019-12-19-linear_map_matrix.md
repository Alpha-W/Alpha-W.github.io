---
layout: post
title: '线性映射与矩阵'
date: 2019-12-19
author: 'Hao Wong'
tags: 代数
---

1.线性映射的矩阵表示

设$V_1$,$V_2$分别为域$F$上的n维与m维线性空间，$\phi\in Hom(V_1,V_2)$.又设矩阵$A$为域$F$上的$m\times n$阶矩阵，即$A\in M_{m\times n}(F)$.定义$\mathcal{A}:F_n\to F_m,x\mapsto Ax$故 $\mathcal{A}\in Hom(F^n,F^m)$.由于$Hom(F^n,F^m)\cong Hom(V_1,V_2)$.我们想到能否用$\mathcal{A}$来表示$\phi$.即能否将一般的线性映射归结为“用矩阵左乘”这样的线性映射?下面证明之.

取定$V_1,V_2$的一组(有序)基$\alpha_1,...,\alpha_n$与$\beta_1,...,\beta_m$.

设$\phi \alpha_j=\sum_{k=1}^m a_{kj}\beta_k=(\beta_1,...,\beta_m)(a_{1j},...,a_{mj})^T$ $(j=1,2,...,n)$ $\phi(\alpha_1,...,\alpha_n)=(\phi\alpha_1,...,\phi\alpha_n)=(\beta_1,...,\beta_m)A$.

$\forall\alpha=(\alpha_1,...,\alpha_n)(x_1,...,x_n)^T,(x_1,...,x_n)^T$为$\alpha$在基$\alpha_1,...,\alpha_n$下的坐标.

$\phi\alpha=(\phi\alpha_1,...,\phi\alpha_n)(x_1,...,x_n)^T=\phi(\alpha_1,...,\alpha_n)(x_1,...,x_n)^T=(\beta_1,...,\beta_m)A(x_1,...,x_n)^T$

即$\phi\alpha$在基$\beta_1,...,\beta_m$下的坐标为$A(x_1,...,x_n)^T$

记$C_1((\alpha_1,...,\alpha_n)(x_1,...,x_n)^T)=(x_1,...,x_n)^T,C_2((\beta_1,...,\beta_m)(x_1,...,x_m)^T)=(x_1,...,x_m)^T$

则有交换图:

$$\require{AMScd}\begin{CD}V_1@>{\phi}>>V_2\\@V{C_1}VV@V{C_2}VV\\F^n@>{\mathcal{A}}>>F^m\end{CD}$$

故有以下定理：

设$\phi\in Hom(V_1,V_2),dimV_1=n,dimV_2=m$.于$V_1.V_2$中分别取定一组(有序)基$\alpha_1,...,\alpha_n$与$\beta_1,...,\beta_m$后,以$\phi\alpha_1,...,\phi\alpha_n$的坐标列作矩阵$A$,即$\phi(\alpha_1,...,\alpha_n)=(\beta_1,...,\beta_m)A$.则$\forall\alpha\in V_1,\beta=A\alpha\Leftrightarrow y=Ax$.其中$x,y$分别为$\alpha,\beta$的坐标列.$A$称为$\phi$的矩阵表示.

2.矩阵的四个空间

设$\mathcal{A}:F_n\to F_m,x\mapsto Ax$的伴随为$\mathcal{A}^\star:F_n\to F_m,x\mapsto Ax$.则有:

$A$的右零空间$=ker\mathcal{A}=\{x\mid Ax=0\}=\{x^T\mid x^TA^T=0\}=ker\mathcal{A}^\star=A^T$的左零空间.

$A$的列空间$=Im\mathcal{A}=<\alpha_1,...,\alpha_n>=<(\alpha_1^T)^T,...,(\alpha_n^T)^T>=Im\mathcal{A}^\star=A^T$的左零空间.

$ker\mathcal{A}\oplus Im\mathcal{A}^\star=F^n$

$ker\mathcal{A}^\star\oplus Im\mathcal{A}=F^m$

3.矩阵的逆，左逆，右逆

$A$列满秩$\Leftrightarrow A$有左逆$\Leftrightarrow\mathcal{A}$是单射,$\mathcal{A}^\star$是满射$\Leftrightarrow$ $dimker\mathcal{A}=0,dimker\mathcal{A}^\star=m-n.dimIm\mathcal{A}=dimIm\mathcal{A}^\star=n.\\ $
$A$行满秩$\Leftrightarrow A$有右逆$\Leftrightarrow\mathcal{A}$是满射,$\mathcal{A}^\star$是单射$\Leftrightarrow$ $dimker\mathcal{A}=n-m,dimker\mathcal{A}^\star=0.dimIm\mathcal{A}=dimIm\mathcal{A}^\star=m.$

$A$可逆$\Leftrightarrow A$有左逆且$A$有右逆
