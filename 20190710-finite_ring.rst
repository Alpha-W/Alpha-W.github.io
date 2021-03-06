==========================
有限环何时是有限域?
==========================
:Author: Hau Wong
:Date:   2019-07-10
:Category: 代数

与有限环相比，有限域的性质要好很多.本文给出3个有限环是有限域的充分条件.

Theorem 1:

有限幺环中只有可逆元与零因子.

Proof:

:math:`R=0`\时,结论平凡. :math:`R\neq 0`\时, :math:`\forall 0 \neq a \in R, R`\为有限幺环,则 :math:`1=a^0,a^1,a^2...`\包含重复项. 设 :math:`a^l=a^n,`\并且n为满足上式的最小数.则有 :math:`n-1 \geq 0`\.以下分两种情形讨论.

① :math:`l=0:1=a^0=a^n=a\cdot a^{n-1}=a^{n-1}\cdot a \Rightarrow a^{n-1}`\是 :math:`a`\的逆元 :math:`\Rightarrow a`\为可逆元.

② :math:`l\gt0:0\le l-1\lt n-1 \Rightarrow0=a\cdot(a^{n-1}-a^{l-1})\Rightarrow a^{n-1}\neq a^{l-1}`\(由 :math:`n`\的最小性) :math:`\Rightarrow a^{n-1}-a^{l-1}\neq 0 \Rightarrow a`\是左零因子.

同理,由 :math:`0=(a^{n-1}-a^{l-1})\cdot a`\可得 :math:`a`\是右零因子.即 :math:`a`\是零因子. 

而当 :math:`a=0`\时, :math:`a`\显然是零因子. 

故综合①②知:有限幺环只有可逆元与零因子.得证.

并且还有以下推论:

Corollary  1:有限整环是域. 

推论1中,交换幺环这个条件太强了,我们分两步去掉这个条件:

Theorem 2:有限除环是域. 

在证明之前,我们先证明一个引理:

Lemma 1:

:math:`\forall d <n \wedge d\mid n , \prod_{(i,n)=1}(x-e^{\frac{2\pi i}{n}})\mid \frac{x^n-1}{x^d-1}`\

Proof:

令 :math:`\Phi_{n}(x)=\prod_{(i,n)=1}(x-e^{\frac{2\pi i}{n}}),`\则有 :math:`x^n-1=\prod_{i=1}^n(x-e^{\frac{2\pi i}{n}})=\prod_{d\mid n}\Phi_{d}(x)=`\  :math:`\Phi_{n}(x)\prod_{d\mid n \atop d<n}\Phi_{d}(x)`\ 

下证 :math:`\forall n \in \mathbb{N＋},\Phi_{n}(x)`\是整系数首一多项式. 因 :math:`\Phi_{1}(x)=x-1`\是整系数首一多项式,设 :math:`\forall m<n,\Phi_{n}(x)`\是整系数首一多项式.则由 :math:`\Phi_{n}(x)=\frac{x^n-1}{\prod_{d\mid n \atop d<n}\Phi_{d}(x)}`\得  :math:`\Phi_{n}(x)`\是整系数首一多项式. 

而注意到 :math:`x^d-1=\prod_{t\mid d}\Phi_{t}(x)\Rightarrow x^n-1=\Phi_{n}(x)(x^d-1)\prod_{k\mid n \wedge k<n\atop k\not\mid d }\Phi_{d}(x)\Rightarrow\Phi_{n}(x)\mid\frac{x^n-1}{x^d-1}`\ ,得证. 

之后我们就可以着手来证明定理2了:

Proof:

设 :math:`D`\是有限除环,则 :math:`D`\是其中心 :math:`C(D)=\{z\in D:za=az,\forall a\in D\}`\上的 :math:`n`\维线性空间,下证 :math:`n=1`\ .

设 :math:`\mid C(D)\mid =q`\,则 :math:`\mid D\mid =q^n`\.记 :math:`D^\times`\为 :math:`D`\中所有可逆元组成的集合,则 :math:`\mid D^\times\mid =q^n-1 \forall a\in D`\,记 :math:`a`\的中心化子 :math:`C(a)=\{x\in D:ax=xa\}`\ ,则有 :math:`C(D)\subset C(a)\Rightarrow C(a)`\是 :math:`C(D)`\上的线性空间. 

:math:`\Rightarrow \mid C(a)\mid =q^d\quad`\ ( :math:`d`\与 :math:`a`\有关) :math:`\Rightarrow \mid C(a)^\times\mid =q^d-1.`\再由 :math:`C(a)^\times\le D^\times得q^d-1|q^n-1.`\ 

下证 :math:`d|n`\ .由带余除法, :math:`n=Qd+r\quad(0\le r<d).`\因 :math:`q^d-1|q^n-1`\,故有 
:math:`q^d-1|(q^n-1)-(q^{n-d}+q^{n-2d}+\ldots+q^{n-Qd})(q^d-1)=q^{n-Qd}-1=q^r-1\Rightarrow q^d-1|q^r-1`\.但 :math:`0\le r<d`\,若 :math:`r>0,q^d-1>q^r-1与q^d-1|q^r-1`\矛盾,故 :math:`r=0\Rightarrow d|n`\

由群方程, :math:`\mid D^\times\mid=\mid C(D^\times)\mid+\sum_{a\not\in C(D^\times)}\frac{\mid D^\times\mid}{C(a)}`\  :math:`\Rightarrow q^n-1=q-1+\sum_{d\mid n \atop d<n}\frac{q^n-1}{q^d-1}`\

再由引理1, :math:`\forall d<n \wedge d\mid n,\Phi_{n}(q)\mid\frac{x^n-1}{x^d-1}\Rightarrow\Phi_{n}(q)\mid q^n-1\Rightarrow\Phi_{n}(q)\mid q-1`\

若 :math:`n>1`\则 :math:`\mid q-e^{\frac{2\pi i}{n}}\mid>q-1,\forall (i,n)=1\Rightarrow\Phi_{n}(q)=\prod_{(i,n)=1}(q-e^{\frac{2\pi i}{n}})>q-1\Rightarrow\Phi_{n}(q)\not\mid q-1`\,矛盾. 

故 :math:`n=1`\,即 :math:`D=C(D),D`\是交换环 :math:`\Rightarrow D`\是域.得证. 

我们已经去掉了交换环这个条件了,下面我们去掉含有幺元的条件:

Theorem 3:

没有非零零因子的非零有限环是域. 

Proof:

:math:`\forall 0 \neq a \in R,\alpha(r)=ra`\是双射.否则, :math:`\exists r_{1}\neq r_{2}\in R`\,使 :math:`r_{1} a=r_{2} a\Rightarrow (r_{1}-r_{2}) a=0\Rightarrow r_{1}=r_{2}`\,矛盾,故 :math:`\exists t,t^\prime \in R`\,使 :math:`a=t a,t^\prime a=t`\.同理 :math:`\beta(r)=ar`\也是双射 :math:`\Rightarrow\exists s,s^\prime \in R`\,使 :math:`a=as,as^\prime =s`\.
则 :math:`\forall x \in R,\exists b,c\in R,x=ba=ac\Rightarrow tx=t(ac)=(ta)c=ac=x\Rightarrow t`\是 :math:`R`\的左幺元 
:math:`xs=(ba)s=b(as)=ba=x \Rightarrow s`\是R的右幺元 :math:`\Rightarrow t=ts=s=1`\是 :math:`R`\的幺元 
再由 :math:`as^\prime =s=1=t=t^\prime a\Rightarrow a`\有右逆元 :math:`s^\prime `\与左逆元 :math:`t^\prime \Rightarrow s^\prime =1s^\prime =(t^\prime a)s^\prime =t^\prime (as^\prime )=t^\prime 1=t^\prime`\
是 :math:`s^\prime`\与 :math:`t^\prime`\为 :math:`a`\的逆元 :math:`\Rightarrow R`\的任意非零元都有逆元 :math:`\Rightarrow R`\是有限除环.由定理2, :math:`R`\是域.得证. 

我们已经知道在有限非零环中由零因子的个数可以得出结论,那么由可逆元的个数有没有对应的结论呢?答案是肯定的，不过要注意的是只有在幺环中才有可逆元这个概念.我们先证一个引理.

Lemma 2: 

设 :math:`R`\是非零有限幺环,若 :math:`R`\的左零因子个数为 :math:`n`\,且 :math:`n>1`\,则有 :math:`\mid R\mid \le n^2`\.

Proof:

:math:`\forall w \in R,`\记 :math:`Ann_{R}(w)=\{r\in R:wr=0\}`\.
由定理1, :math:`R`\的右零因子个数为 :math:`n`\,故 :math:`\exists 0\ne x\in R`\,使 :math:`1<\mid Ann_{R}(x)\mid\le n \forall 0\ne y\in Ann_{R}(x)`\,因 :math:`x(yr)=(xy)r`\,故 :math:`yR\le Ann_{R}(x)`\,即 :math:`\mid yR\mid\le n
\forall r \in R`\,设 :math:`f(r)=yr`\.由左分配律, :math:`f`\是群 :math:`\{R,+\}`\到群 :math:`\{yR,+\}`\的满同态.而 :math:`Kerf=Ann_{R}(y)`\,故 :math:`R/Ann_{R}(y)\cong yR \Rightarrow\mid R\mid=\mid Ann_{R}(y)\mid\times\mid yR\mid\le n\times n=n^2`\.得证

Theorem 4:

设 :math:`R`\是非零有限幺环, :math:`T`\是 :math:`R`\中所有可逆元组成的集合.若 :math:`\mid T\mid >\mid R\mid-\sqrt{\mid R\mid}`\,则 :math:`R`\是域.

Proof:

由定理1, :math:`R-T`\为 :math:`R`\中所有零因子组成的集合.故有 :math:`\mid T\mid +\mid R-T\mid=\mid R\mid.`\若 :math:`R-T=\{0\}`\,则由定理2, :math:`R`\是域．否则,设 :math:`\mid R-T\mid>1`\,则由引理2, :math:`\mid R\mid\le \mid R-T\mid^2 \Rightarrow \sqrt{\mid R\mid}\le \mid R-T\mid =\mid R\mid-\mid T\mid \Rightarrow \mid T\mid\le\mid R\mid -\sqrt{\mid R\mid }`\与 :math:`\mid T\mid>\mid R\mid -\sqrt{\mid R\mid}`\矛盾,故 :math:`R-T=\{0\}`\,即 :math:`R`\是域.得证 

综上,设 :math:`T`\是 :math:`R`\中所有可逆元组成的集合, :math:`D`\是 :math:`R`\中所有零因子组成的集合,我们有如下定理:

Theorem 5:

若 :math:`R`\是非零有限环,且满足下列条件之一:

①: :math:`\mid D\mid=1`\

②: :math:`R`\是幺环且 :math:`\mid T\mid>\mid R\mid-\sqrt{\mid R\mid}`\

③: :math:`R`\是幺环且 :math:`\mid D|<\sqrt{\mid R|}`\

则 :math:`R`\是域.
