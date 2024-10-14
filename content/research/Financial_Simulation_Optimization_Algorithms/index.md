---
title: Research on Financial Simulation Optimization Algorithms
summary: Black Optimization, Simulation
date: 2024-05-30
type: docs
math: false
tags:
  - Optimization
image:
  caption: 'Embed rich media such as videos and LaTeX math'
---
<!-- 
I am currently focused on conducting a comprehensive literature review, summarizing multiple research papers and presenting findings to my supervisor Prof. Yang. In terms of experimentation, I have completed the initial step of applying Monte Carlo Bayesian optimization to stock midprice modeling. The ongoing work involves integrating neural networks as surrogate models to further enhance the optimization process.
## 1. Introduction
### (1) Motivation:

The primary motivation for this study is to construct a parallel simulation system that replicates a real-world financial market. By ensuring the high fidelity of the simulation system, we can effectively model the real market. The ultimate goal is to use this system for counterfactual analysis—by intervening in the simulated market, we can predict potential changes, assisting businesses and governments in making informed decisions.

### (2) Research Questions:

One practical approach to achieving this is to optimize the simulation system's parameters, such that the system can replicate real-world market observations. This presents a complex optimization challenge, especially given that the simulation system often consists of multiple intelligent agents, each representing different social actors (e.g., market traders). As the number of agents grows, the problem escalates into a high-dimensional optimization task, essentially a black-box optimization problem.

## 2. Background and Literature Review

#### (1) Bayesian Methods and Their Variants:

Bayesian methods have long been employed in high-dimensional optimization, offering a probabilistic framework for modeling uncertainty. Variants of these methods have been developed to handle complex, high-dimensional problems more effectively, leveraging prior knowledge about the system.

#### (2) Random Embeddings:

One of the early approaches to high-dimensional Bayesian optimization is Random Embeddings (RE). The core idea is to project the high-dimensional space onto a lower-dimensional subspace using randomly generated projection matrices. Numerous studies provide rigorous mathematical proofs demonstrating the algorithm's invariance to the addition of irrelevant dimensions and rotations.

#### (3) Neural Network Surrogate Models:

Recent advancements in neural network-based surrogate models show promise in addressing high-dimensional problems more efficiently. Neural networks, through amortized training, allow for inference in high-dimensional spaces with just a single forward pass, avoiding the prohibitive complexity of traditional methods. This opens the possibility of extending Bayesian Optimization (BO) to high-dimensional problems without relying on external dimensionality reduction techniques like RE.

A potential approach involves using normalizing flows to model the high-dimensional parameters of a financial market. Additionally, a discriminator can be employed to distinguish between simulated and real data for calibration. This could also be extended to use a Generative Adversarial Network (GAN), where the generator produces market parameters and the discriminator evaluates the calibration accuracy against real data. The goal is to develop an automated calibration system using these advanced neural network architectures.

## 3. Data Description

The dataset for this study is sourced from Ping An Bank, a leading financial institution in China. A simulator has already been developed by the research group, providing the necessary environment for testing the optimization methods. The remaining task is to implement the optimization methods for this black-box optimization problem.

## 4. Methodology

To initiate this study, a Monte Carlo Approximate Bayesian Computation (ABC) method has been implemented as a preliminary approach. This serves as a baseline for testing the optimization framework. The next step involves implementing a neural network-based optimization method to enhance the system's performance. The goal is to leverage the neural network's ability to handle high-dimensional parameter spaces and create an efficient, automated calibration system.

## Reference
1. Chen, Yutian. Learning to learn without gradient descent by gradient descent (2016).
2. Frazier, Peter I. A Tutorial on Bayesian Optimization (2018).
3. Wang, Ziyu. Bayesian Optimization in a Billion Dimensions via Random Embeddings (2016).
4. Cranmer, Kyle. The Frontier of Simulation-Based Inference (2020).
5. Lueckmann, Jan-Matthis. Benchmarking Simulation-Based Inference (2021).
6. Dai, Zhongxiang. Sample-Then-Optimize Batch Neural Thompson Sampling (2022). -->

<!-- [Hugo Blox Builder](https://hugoblox.com) is designed to give technical content creators a seamless experience. You can focus on the content and the Hugo Blox Builder which this template is built upon handles the rest.

**Embed videos, podcasts, code, LaTeX math, and even test students!**

On this page, you'll find some examples of the types of technical content that can be rendered with Hugo Blox.

## Video

Teach your course by sharing videos with your students. Choose from one of the following approaches:

{{< youtube D2vj0WcvH5c >}}

**Youtube**:

    {{</* youtube w7Ft2ymGmfc */>}}

**Bilibili**:

    {{</* bilibili id="BV1WV4y1r7DF" */>}}

**Video file**

Videos may be added to a page by either placing them in your `assets/media/` media library or in your [page's folder](https://gohugo.io/content-management/page-bundles/), and then embedding them with the _video_ shortcode:

    {{</* video src="my_video.mp4" controls="yes" */>}}

## Podcast

You can add a podcast or music to a page by placing the MP3 file in the page's folder or the media library folder and then embedding the audio on your page with the _audio_ shortcode:

    {{</* audio src="ambient-piano.mp3" */>}}

Try it out:

{{< audio src="ambient-piano.mp3" >}}

## Test students

Provide a simple yet fun self-assessment by revealing the solutions to challenges with the `spoiler` shortcode:

```markdown
{{</* spoiler text="👉 Click to view the solution" */>}}
You found me!
{{</* /spoiler */>}}
```

renders as

{{< spoiler text="👉 Click to view the solution" >}} You found me 🎉 {{< /spoiler >}}

## Math

Hugo Blox Builder supports a Markdown extension for $\LaTeX$ math. You can enable this feature by toggling the `math` option in your `config/_default/params.yaml` file.

To render _inline_ or _block_ math, wrap your LaTeX math with `{{</* math */>}}$...${{</* /math */>}}` or `{{</* math */>}}$$...$${{</* /math */>}}`, respectively.

{{% callout note %}}
We wrap the LaTeX math in the Hugo Blox _math_ shortcode to prevent Hugo rendering our math as Markdown.
{{% /callout %}}

Example **math block**:

```latex
{{</* math */>}}
$$
\gamma_{n} = \frac{ \left | \left (\mathbf x_{n} - \mathbf x_{n-1} \right )^T \left [\nabla F (\mathbf x_{n}) - \nabla F (\mathbf x_{n-1}) \right ] \right |}{\left \|\nabla F(\mathbf{x}_{n}) - \nabla F(\mathbf{x}_{n-1}) \right \|^2}
$$
{{</* /math */>}}
```

renders as

{{< math >}}
$$\gamma_{n} = \frac{ \left | \left (\mathbf x_{n} - \mathbf x_{n-1} \right )^T \left [\nabla F (\mathbf x_{n}) - \nabla F (\mathbf x_{n-1}) \right ] \right |}{\left \|\nabla F(\mathbf{x}_{n}) - \nabla F(\mathbf{x}_{n-1}) \right \|^2}$$
{{< /math >}}

Example **inline math** `{{</* math */>}}$\nabla F(\mathbf{x}_{n})${{</* /math */>}}` renders as {{< math >}}$\nabla F(\mathbf{x}_{n})${{< /math >}}.

Example **multi-line math** using the math linebreak (`\\`):

```latex
{{</* math */>}}
$$f(k;p_{0}^{*}) = \begin{cases}p_{0}^{*} & \text{if }k=1, \\
1-p_{0}^{*} & \text{if }k=0.\end{cases}$$
{{</* /math */>}}
```

renders as

{{< math >}}

$$
f(k;p_{0}^{*}) = \begin{cases}p_{0}^{*} & \text{if }k=1, \\
1-p_{0}^{*} & \text{if }k=0.\end{cases}
$$

{{< /math >}}

## Code

Hugo Blox Builder utilises Hugo's Markdown extension for highlighting code syntax. The code theme can be selected in the `config/_default/params.yaml` file.


    ```python
    import pandas as pd
    data = pd.read_csv("data.csv")
    data.head()
    ```

renders as

```python
import pandas as pd
data = pd.read_csv("data.csv")
data.head()
```

## Inline Images

```go
{{</* icon name="python" */>}} Python
```

renders as

{{< icon name="python" >}} Python

## Did you find this page helpful? Consider sharing it 🙌 -->
