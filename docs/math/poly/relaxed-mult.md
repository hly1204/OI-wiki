在 [快速傅里叶变换](./fft.md) 和 [快速数论变换](./ntt.md) 中我们已经介绍了如何完成 **离线** 的多项式乘法，在这里我们会简单介绍如何完成 **在线** 的多项式乘法。

该算法常用来计算一些隐式定义的幂级数的截断，例如用公式 $\mathrm{e}^{h} = \int h'\mathrm{e}^h$ 来计算 $\mathrm{e}^h$，其中 $h \in \mathbb{C}\left[\left[x\right]\right], h(0) = 0$。

该算法由 Hoeven 在 1997 年首次介绍并给出了时间复杂度为 $O(\mathsf{M}(n)\log(n))$ 的算法，其中 $\mathsf{M}(n)$ 为两个次数小于 $n$ 的多项式相乘的时间。后来时间复杂度也由 Hoeven 进行过若干次改进，但是改进后的算法在算法竞赛中一般由于数据范围限制不太实用且更加复杂，所以我们只会简单介绍前者。

后文我们将使用 radix-2 FFT/NTT 并结合 Middle Product 算法来计算一部分多项式乘法。

## 定义

### 半在线乘法

#### Middle Product

### 在线乘法

## 参考文献

1. Joris van der Hoeven. 1997. [Lazy multiplication of formal power series](https://doi.org/10.1145/258726.258738). In Proceedings of the 1997 international symposium on Symbolic and algebraic computation (ISSAC '97). Association for Computing Machinery, New York, NY, USA, 17–20.
2. Joris van der Hoeven. [Relax, but Don’t be Too Lazy](https://doi.org/10.1006/jsco.2002.0562). Journal of Symbolic Computation. Volume 34, Issue 6, 2002, Pages 479-542, ISSN 0747-7171.
3. Romain Lebreton, Éric Schost. [A simple and fast online power series multiplication and its analysis](https://hal-lirmm.ccsd.cnrs.fr/lirmm-00867279v2). Journal of Symbolic Computation, 2016, 72, pp.231-251. ⟨10.1016/j.jsc.2015.03.001⟩. ⟨lirmm-00867279v2⟩
4. Guillaume Hanrot, Michel Quercia, Paul Zimmermann. [The Middle Product Algorithm, I.](https://hal.science/inria-00071921). [Research Report] RR-4664, INRIA. 2002. ⟨inria-00071921⟩
