---
title: 统计建模与概率论基础测试
date: 2026-02-14 18:00:00
tags:
  - 概率论
  - 统计模型
categories:
  - 数学基础
mathjax: true
cover: https://images.unsplash.com/photo-1509228468518-180dd4864904?ixlib=rb-1.2.1&auto=format&fit=crop&w=1000&q=80
---

# 概率分布与参数估计

这是一篇用于测试 Hexo 博客数学公式渲染（MathJax）的极客文档。如果你能正确看到下面的公式且没有乱码，说明你的渲染引擎和插件配置已经彻底大功告成！

## 1. 正态分布 (Normal Distribution)

正态分布是统计学中最重要的一种连续概率分布。其概率密度函数的行内公式为 $X \sim N(\mu, \sigma^2)$，对应的块级公式如下：

$$
f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}
$$

其中：
* $\mu$ 代表数学期望（均值），决定了分布的中心位置。
* $\sigma$ 代表标准差，决定了分布的离散程度。
* $\sigma^2$ 代表方差。

## 2. 极大似然估计 (Maximum Likelihood Estimation)

对于独立同分布的样本集 $D = \{x_1, x_2, ..., x_n\}$，其似然函数 $L(\theta)$ 定义为联合概率密度：

$$
L(\theta) = \prod_{i=1}^{n} p(x_i | \theta)
$$

为了防止连乘导致数值下溢，并简化求导计算，我们通常对目标函数取对数，得到对数似然函数（Log-Likelihood）：

$$
\ln L(\theta) = \sum_{i=1}^{n} \ln p(x_i | \theta)
$$

求解参数 $\theta$ 的过程，就是寻找使得上述目标函数取得最大值的参数值。

## 3. 复杂矩阵与多行对齐公式

最后我们来测试一下在模型推导过程中极其常用的多行对齐公式（注意观察等号是否完美对齐）：

$$
\begin{aligned}
\nabla_{\boldsymbol{\theta}} J(\boldsymbol{\theta}) &= \frac{1}{m} \sum_{i=1}^{m} \nabla_{\boldsymbol{\theta}} \mathcal{L}(f(x^{(i)}; \boldsymbol{\theta}), y^{(i)}) \\
&= \frac{1}{m} \mathbf{X}^T (\mathbf{X}\boldsymbol{\theta} - \mathbf{y})
\end{aligned}
$$

---
> 如果上面的三个大公式以及行内变量都能完美显示，恭喜你，你的博客已经具备了排版硬核学术笔记的全部能力！