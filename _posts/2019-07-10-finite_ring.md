---
layout: post
title: '有限环何时是有限域?'
date: 2019-07-10
author: 'Hao Wong'
tags: 代数
---

与有限环相比，有限域的性质要好很多.本文给出3个有限环是有限域的充分条件.



Theorem 1:

有限幺环中只有可逆元与零因子.



Proof:

$R=0$时,结论平凡.$R\neq0$时,$\forall 0 \neq a \in R, R$为有限幺环,则$1=a^0,a^1,a^2...$包含重复项. 设$a^l=a^n,$并且n为满足上式的最小数.则有$n-1 \geq 0$.以下分两种情形讨论.
$①l=0:1=a^0=a^n=a\cdot a^{n-1}=a^{n-1}\cdot a \Rightarrow a^{n-1}$是$a$的逆元$\Rightarrow a$为可逆元.
$②l\gt0:0\le l-1\lt n-1 \Rightarrow0=a\cdot(a^{n-1}-a^{l-1})\Rightarrow a^{n-1}\neq a^{l-1}($由$n$的最小性)$\Rightarrow a^{n-1}-a^{l-1}\neq 0 \Rightarrow a$是左零因子.
同理,由$0=(a^{n-1}-a^{l-1})\cdot a　$可得$a$是右零因子.即$a$是零因子. 
而当$a=0$时,$a$显然是零因子. 
故综合①②知:有限幺环只有可逆元与零因子.得证.

并且还有以下推论:



Corollary  1:

有限整环是域. 



推论1中,交换幺环这个条件太强了,我们分两步去掉这个条件:



Theorem 2:

有限除环是域. 



在证明之前,我们先证明一个引理:



Lemma 1:

$\forall d <n \wedge d\mid n , \prod_{(i,n)=1}(x-e^{\frac{2\pi i}{n}})\mid \frac{x^n-1}{x^d-1} $



Proof:

令$\Phi_{n}(x)=\prod_{(i,n)=1}(x-e^{\frac{2\pi i}{n}}),$则有$x^n-1=\prod_{i=1}^n(x-e^{\frac{2\pi i}{n}})=\prod_{d\mid n}\Phi_{d}(x)=$$\Phi_{n}(x)\prod_{d\mid n \atop d<n}\Phi_{d}(x)$ 
下证$\forall n \in \mathbb{N＋},\Phi_{n}(x)$是整系数首一多项式. 因$\Phi_{1}(x)=x-1$是整系数首一多项式,设$\forall m<n,\Phi_{n}(x)$是整系数首一多项式.则由$\Phi_{n}(x)=\frac{x^n-1}{\prod_{d\mid n \atop d<n}\Phi_{d}(x)}$得 $\Phi_{n}(x)$是整系数首一多项式. 
而注意到$x^d-1=\prod_{t\mid d}\Phi_{t}(x)\Rightarrow x^n-1=\Phi_{n}(x)(x^d-1)\prod_{k\mid n \wedge k<n\atop k\not\mid d }\Phi_{d}(x)\Rightarrow\Phi_{n}(x)\mid\frac{x^n-1}{x^d-1},$得证. 

之后我们就可以着手来证明定理2了:

Proof:

 设$D$是有限除环,则$D$是其中心$C(D)=\{z\in D:za=az,\forall a\in D\}$上的$n$维线性空间,下证$n=1.$ 
设$|C(D)|=q,$则$|D|=q^n.记D^\times$为$D$中所有可逆元组成的集合,则$|D^\times|=q^n-1 \forall a\in D,$记$a$的中心化子$C(a)=\{x\in D:ax=xa\},$则有$C(D)\subset C(a)\Rightarrow C(a)$是$C(D)$上的线性空间. 
$\Rightarrow |C(a)|=q^d\quad(d与a有关)\Rightarrow |C(a)^\times|=q^d-1.$再由$C(a)^\times\le D^\times得q^d-1|q^n-1.$ 
下证$d|n. $由带余除法$,n=Qd+r\quad(0\le r<d).$因$q^d-1|q^n-1,$故有 
$q^d-1|(q^n-1)-(q^{n-d}+q^{n-2d}+\ldots+q^{n-Qd})(q^d-1)=$$q^{n-Qd}-1=q^r-1 
\Rightarrow q^d-1|q^r-1.$但$0\le r<d,若r>0,q^d-1>q^r-1与q^d-1|q^r-1$矛盾,故$r=0\Rightarrow d|n $
由群方程:$|D^\times|=|C(D^\times)|+\sum_{a\not\in C(D^\times)}\frac{|D^\times|}{C(a)}\Rightarrow q^n-1=q-1+\sum_{d\mid n \atop d<n}\frac{q^n-1}{q^d-1} $
再由引理1:$\forall d <n \wedge d\mid n , \Phi_{n}(q)\mid \frac{x^n-1}{x^d-1}\Rightarrow\Phi_{n}(q)\mid q^n-1\Rightarrow\Phi_{n}(q)\mid q-1 
$若$n>1$则$|q-e^{\frac{2\pi i}{n}}|>q-1,\forall (i,n)=1\Rightarrow\Phi_{n}(q)=\prod_{(i,n)=1}(q-e^{\frac{2\pi i}{n}})>q-1\Rightarrow\Phi_{n}(q)\not\mid q-1,$矛盾. 
故$n=1,$即$D=C(D),D$是交换环$\Rightarrow D$是域.得证. 


我们已经去掉了交换环这个条件了,下面我们去掉含有幺元的条件:



Theorem 3:

没有非零零因子的非零有限环是域. 



Proof:

$\forall 0 \neq a \in R,\alpha(r)=ra$是双射.否则$,\exists  r_{1}\neq r_{2}\in R,$使$r_{1} a=r_{2} a\Rightarrow$ $(r_{1}-r_{2}) a=0\Rightarrow r_{1}=r_{2},$矛盾,故$ \exists t,t^\prime \in R,使a=t a,t^\prime a=t.$同理$\beta(r)=ar$也是双射$\Rightarrow\exists s,s^\prime \in R,使a=as,as^\prime =s. $
则$\forall x \in R,\exists b,c\in R,x=ba=ac\Rightarrow tx=t(ac)=(ta)c=ac=x\Rightarrow t$是$R$的左幺元 
$xs=(ba)s=b(as)=ba=x \Rightarrow s$是R的右幺元$ \Rightarrow t=ts=s=1$是$R$的幺元 
再由$as^\prime =s=1=t=t^\prime a\Rightarrow a$有右逆元$s^\prime $与左逆元$t^\prime \Rightarrow s^\prime =1s^\prime =(t^\prime a)s^\prime =t^\prime (as^\prime )=t^\prime 1=t^\prime  $
是$s^\prime $与$t^\prime $为$a$的逆元$\Rightarrow R$的任意非零元都有逆元$\Rightarrow R$是有限除环.由定理2,$R$是域.得证. 

我们已经知道在有限非零环中由零因子的个数可以得出结论,那么由可逆元的个数有没有对应的结论呢?答案是肯定的，不过要注意的是只有在幺环中才有可逆元这个概念.我们先证一个引理.



Lemma 2: 

设$R$是非零有限幺环,若$R$的左零因子个数为$n,$且$n>1,$则有$\mid R\mid \le n^2.$



Proof:

  $\forall w \in R,$记$Ann_{R}(w)=\{r\in R:wr=0\}.$
 由定理1,$R$的右零因子个数为$n,$故$\exists 0\ne x\in R,$使$1<$|$Ann_{R}(x)$|$\le n 
  \forall 0\ne y\in Ann_{R}(x),$因$x(yr)=(xy)r,$故$yR\le Ann_{R}(x),$即$|yR|\le n
  \forall r \in R,$设$f(r)=yr.$由左分配律,$f$是群$\{R,+\}$到群$\{yR,+\}$的满同态.而$Kerf=Ann_{R}(y),$故$R/Ann_{R}(y)\cong yR \Rightarrow$|$R$|$=$|$Ann_{R}(y)$|$\times$|$yR$|$\le n\times n=n^2.$得证



Theorem 4:

设$R$是非零有限幺环,$T$是$R$中所有可逆元组成的集合.若$\mid T\mid >\mid R\mid-\sqrt{\mid R\mid},$则$R$是域.



Proof:


  由定理1,$R-T$为$R$中所有零因子组成的集合.故有$\mid T\mid +\mid R-T\mid=\mid R\mid.$若$R-T=\{0\},$则由定理2,$R$是域．否则,设$\mid R-T\mid>1,$则由引理2,$\mid R\mid\le \mid R-T\mid^2 \Rightarrow \sqrt{\mid R\mid}\le \mid R-T\mid =\mid R\mid-\mid T\mid \Rightarrow \mid T\mid\le\mid R\mid -\sqrt{\mid R\mid }$与$\mid T\mid>\mid R\mid -\sqrt{\mid R\mid}$矛盾,故$R-T=\{0\},$即$R$是域.得证 

综上,设$T$是$R$中所有可逆元组成的集合,$D$是$R$中所有零因子组成的集合,我们有如下定理:



Theorem 5:

若$R$是非零有限环,且满足下列条件之一:
							①:$|D|=1$
							②:$R$是幺环且$|T|>|R|-\sqrt{|R|}$
							③:$R$是幺环且$|D|<\sqrt{|R|}$
则$R$是域.