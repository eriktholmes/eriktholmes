
<h1 align="center"> Erik Holmes </h1>
<h3 align="center">   Mathematics | Machine Learning | Research  </h3>

<br>

  | <sub>⚠️ Disclaimer:  This GitHub is part learning journal, part research sandbox — evolving (sometimes daily 🤞) as I work through various projects. It’s a bit nerdy, occasionally verbose, and sometimes a little chaotic, but the goal is simple: build toward interpretability from the ground up.</sub>| 
  | --------- | 
<br>

### About me: 
I am currently a postdoctoral fellow at the University of Toronto working in number theory/arithmetic statistics, and am transitioning into industry. As a mathematician, I have always been drawn to computational methods and have used Python throughout my career to generate, analyze, and visualize data. More generally, I try to write code to help visualize and build intuition around mathematical objects. 

My current focus is on machine learning where-with the rapid growth of AI-I find myself thinking often about safety and the potential impacts this field has on society. As such, I am increasingly interested in **interpretability** and **alignment** though I am certainly still in an exploratory phase. 
***Ultimately**, I hope to contribute to safe, understandable AI systems and to apply my research experience in pure math to problems that have an immediate impact.*

> 🎥 *Fun fact: I worked as a video editor for a short while during grad school and have a deep love and respect for storytellers. Sometimes this promotes an overly verbous style of writing on my behalf.*

<br> 


## 🎯 Goals:
> Building toward an interpretability/safety-focused ML research or engineering role by August 2025.
#### 🔍 Current (Summer 2025):
- Rebuild core ML models from scratch (micrograd, character-level language models (makemore), transformers)
- Analyze internals of trained networks (e.g., MLPs/CNNs on MNIST)
- Explore toy RL setups (AlphaZero-lite, MCTS agents)
- Start working with tools like TransformerLens


#### 🔭 Long-Term:
- Contribute to safe, interpretable AI systems
- Work at the intersection of math, ML, and alignment
- Apply my research skills to problems with real-world impact


<!--
- 📚 I am working to understand foundational concepts and interpretability through ML projects and courses: for example project builds like [micrograd](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode-1/micrograd),  [makemore](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode_2), and (*currently the skeleton of*) [AlphaZero lite](https://github.com/eriktholmes/ai_sandbox). 
  - these toy problems led me to port the micrograd approach to PyTorch, train a basic classifier on MNIST data and analyze neuron behavior through pixel activation maps.
    - [HERE](https://github.com/eriktholmes/educational_notebooks/blob/main/mlp_explained_pytorch.ipynb) I spend an afternoon writing a basic overview of MLPs from this micrograd perspective.  
- 📈 Long-term learning goals/research interests: interpretability, alignment, and AI safety.
  - Baby steps towards this is a repo specifically designed for [interpretabilty](https://github.com/eriktholmes/interpreting_mnist) of models trained on MNIST.
- ✍️ Also I am still working on various [research projects](https://erikholmesmath.com/research.htm) in number theory. 
-->

<br> 

## 🪚 Current work
- 🔧 [micrograd](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode-1), [makemore](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode_2): foundational deep learning models, built for hands-on learning
- 🔬 [interpreting_mnist](https://github.com/eriktholmes/interpreting_mnist/tree/main/MLP): exploratory repo on internal neuron behavior (activation drift, normalization effects, etc.)
- 🧠 [mlp_explained_pytorch](https://github.com/eriktholmes/educational_notebooks/blob/main/mlp_explained_pytorch.ipynb): breakdown of an MLP in PyTorch, inspired by the micrograd build
- 🎲 [ai_sandbox](https://github.com/eriktholmes/ai_sandbox): experimental repo, currently looking at reinforcement learning environments and AlphaZero-style agents
- 🔣 [Number theory research](https://erikholmesmath.com/research.htm): ongoing collaborations on lattices in number fields, and in how their geometry varies within *natural* families. 





<br> 
<br> 

## 📌 Featured (ML related) Repositories

### [`Zero-to-hero-course`](https://github.com/eriktholmes/Zero-to-hero-course)
A walkthrough of Andrej Karpathy’s Zero to Hero YouTube series. Includes:
- A build of [micrograd](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode-1/micrograd)
- Experiments on custom activations, and attempts at understanding neuron activations
- Exploratory/blog-style notes and diagrams (with more to come!)
- Currently in progress: [makemore](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode_2), a character-level language model inspired by Karpathy’s series. So far, we've implemented a bigram model that predicts the next character from the previous one, trained on the names dataset. Next, we are extending this to a flexible context window model that utilizes multiple preceding characters. Along the way, we are incorporating techniques from later episodes—like improved optimization strategies and training intuition. For readers interested in interpretability and training dynamics (e.g., why normalization matters), see also the interpreting_mnist repo below.
---
### [`interpreting_mnist`](https://github.com/eriktholmes/interpreting_mnist)
The goal: to interpret models trained on MNIST. While the dataset and models are intentionally simple, the goal is to build and document real interpretability tools — starting from first principles and scaling up. 

So far the repo will be organized into two tracks: the `MLP` and the `CNN`.
#### :one: [`MLP`](https://github.com/eriktholmes/interpreting_mnist/tree/main/MLP):
 - Our [first notebook](https://github.com/eriktholmes/interpreting_mnist/blob/main/MLP/01_MLP_for_Interpretability_non_normalized.ipynb) investigates the effects of training an MLP on non-normalized MNIST data. By manually logging activations during the forward pass, we track how internal representations evolve over time.\
**Observations:**
    - Significant mean drift and growing variance in early layer activations
    - Class based activation statistics reveal internal instability, despite strong test performance (~94–97%)
    - Clear motivation for normalization techniques to improve training!
    > The goal with this first notebook is to motivate deeper interpretability tools (e.g., activation hooks, PCA, gradient tracking), and provide a foundation for exploring how neural networks process and separate information — one layer at a time.
---

### [```ai_sandbox```](https://github.com/eriktholmes/ai_sandbox) 
This is another, less structured, space for ML/AI experiments:
- Currently working on the basics towards AlphaZero: build game environments for TicTacToe and Connect Four, and implemented basic Monte Carlo Tree Search for Tic Tac Toe.
  - Ran simple experiements such as two players moving at random, random vs MCTS, random vs Greedy play, etc.
  - (more to come)

<!--
### [`Math_things`](https://github.com/eriktholmes/math_things)
A catch-all for math-related code, currently focused on:
- Computational experiments related to unit lattices in number fields
- Visualization of rank 2 shapes within the [fundamental domain](/Math_things/unit_shapes/FD_domain.png)
- Ongoing research on lattices and questions of distribution
- Ultimately, I am excited about a possible application of lattice shapes to log terms in Malle's conjecture (which is roughly about the asymptotics of specialized counting functions) and hope to have some code related to that at some point...?
-->



<br> 
<br> 

## 🔗 Contact & More
- 📫 eriktholmes@gmail.com
- 🌐 [erikholmesmath.com](https://erikholmesmath.com)


<!---
eriktholmes/eriktholmes is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
