
<h1 align="center"> Erik Holmes </h1>
<h3 align="center">   Mathematics | Machine Learning | Research  </h3>

<br>

  | <sub>⚠️ Disclaimer: This GitHub is part learning journal/blog, part experimental sandbox — evolving as I work through various projects. It's a bit nerdy, occasionally verbose, and sometimes a little chaotic — but the goal is to build a rigorous foundation in maachine learning with a focus on interpretability and alignment.</sub>| 
  | --------- | 
<br>

# About Me

I’m a mathematician and postdoctoral researcher at the University of Toronto, with a focus on computational methods in number theory and arithmetic statistics and am transitioning into AI/ML. My focus is on mechanistic interpretability, alignment, and safe AI systems — applying a decade of mathematical research experience to build models that are both powerful and understandable.

I bring:

- **PhD in mathematics** — 10+ years of abstraction, proof, and computational research
- **Strong Python & PyTorch skills** — from-scratch builds, reproducible experiments
- **Research-driven mindset** — blending theory, computation, and clear communication

Beyond the technical side, I care deeply about using AI to foster community and human connection rather than diminish it.

*Ultimately*: I want to help push the boundaries of AI while keeping it safe, interpretable, and human-centered.


<!--
## 🤔 My Research Philosophy
Broadly, I enjoy project based learning: in mathematics I like to start with 'toy' problems (low dimensional case analysis), focus on visualizations whenever possible, and try to build intuition and tools based on computational exploratation. By starting small and understanding the mechanisms at work questions naturally arise, and these often involve learning/understanding/developing new tools to solve. I am taking the same approach with ML. Some key words that describe my ideals:
- **Application-driven**: I’m most excited when theory connects to something tangible and impactful.
- **Computational explorator**: In both mathematics and ML, I use computation to probe abstract structures, uncover patterns, and build intuition from the ground up.
- **Focused on interpretability & alignment**: The rapid evolution of AI — and its societal impact — drew me to these areas, where better tools and understanding can directly lead to safer, more capable models.


> **Fun fact**: Before academia, I worked in residential construction in the U.S. and Canada, and later as a video editor in Hawaii.


<br>





📚 ➕ 🧪 **I enjoy work that blends theory with experimentation and am driven by applications**:
   
  - Most of my research involves using computational tools to explore abstract structures. I really enjoy the process—digging into patterns, testing ideas, and building intuition from the ground up.
  - While I do love math, I’ve found I’m most energized when research connects to something more tangible. With AI advancing quickly and showing up in nearly every domain, I decided to shift gears.
  - I’ve been especially drawn to interpretability, alignment, and the challenge of building systems we can actually trust.

**Ultimately**, I want to contribute to safe, understandable AI—and to bring the rigor of mathematics to problems with real-world applications and urgency.

> Fun fact: Before academia, I worked in residential construction (helped build homes in the U.S. and Canada) and later as a video editor on various small projects in Hawaii. I like building things—whether out of wood, images, or code.

<br> 

## About this github:
Most of my repos involve small from-scratch builds, visualizations (whenever possible), and interpretability experiments. The hope is that they are readable (albeit a bit long at times), testable, and useful for learning — both mine and yours. More about my approach [here](https://github.com/eriktholmes/eriktholmes/blob/main/learning_approach.md).

<br> 
-->


## 🎯 Goals

> Building toward an interpretability/safety-focused ML research or engineering role by **2026**.

### 🔍 Current Focus (Summer 2025)
- Master core architectures by rebuilding micrograd, makemore, and a minimal GPT from scratch — deepening understanding of training dynamics and attention.
- Analyze vision model internals via neuron selectivity, ablation, activation drift, and PCA/UMAP subspace analysis on MNIST MLP/CNNs.
- Develop toy RL agents with AlphaZero-lite (e.g., Connect Four) using Monte Carlo Tree Search and policy/value networks.
- Apply Transformer interpretability tools, focusing on TransformerLens experiments.
- Investigate fine-tuning effects on representation space, tracking neuron shifts, attention patterns, and decision boundaries.

### 🔭 Long-Term
- Contribute to safe, interpretable AI systems.
- Apply math/ML hybrid skills to impactful, real-world problems.
- Collaborate on research that bridges theory and applied ML.


---

<!--
- 📚 I am working to understand foundational concepts and interpretability through ML projects and courses: for example project builds like [micrograd](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode-1/micrograd),  [makemore](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode_2), and (*currently the skeleton of*) [AlphaZero lite](https://github.com/eriktholmes/ai_sandbox). 
  - these toy problems led me to port the micrograd approach to PyTorch, train a basic classifier on MNIST data and analyze neuron behavior through pixel activation maps.
    - [HERE](https://github.com/eriktholmes/educational_notebooks/blob/main/mlp_explained_pytorch.ipynb) I spend an afternoon writing a basic overview of MLPs from this micrograd perspective.  
- 📈 Long-term learning goals/research interests: interpretability, alignment, and AI safety.
  - Baby steps towards this is a repo specifically designed for [interpretabilty](https://github.com/eriktholmes/interpreting_mnist) of models trained on MNIST.
- ✍️ Also I am still working on various [research projects](https://erikholmesmath.com/research.htm) in number theory. 
-->



<br> 
<br> 

# 📌 Featured (ML related) Repositories

## [`interpreting_mnist`](https://github.com/eriktholmes/interpreting_mnist)
Neuron-level interpretability experiments on MLP/CNN classifiers trained on MNIST.
- **Methods**: activation tracking, selectivity scoring, ablations, activation drift, PCA/UMAP visualization of feature subspaces.
- **Key finding**: Discovered “bottleneck neurons” — ablating a single neuron reduced accuracy on digit “6” to 0%, while leaving others mostly unaffected.
- Includes annotated notebooks, visualizations, and upcoming CNN/Transformer comparisons.
  
  > <img width="400" height="300" alt="Screenshot 2025-08-06 at 11 39 05 AM" src="https://github.com/user-attachments/assets/8b857c5d-a2e7-4ab3-9fdb-d60a60bee24d" />
  >
  > <sub>Scaling a single neuron’s activation boosts accuracy on digit “8” while leaving other classes (mostly) unchanged</sub>
---


## [`ml-fundamentals`](https://github.com/eriktholmes/ml-fundamentals-from-scratch)
From-scratch implementations of key deep learning building blocks — from a scalar autograd engine (`micrograd`) to a mini GPT trained on Robert Frost’s poetry.
**Highlights**:
- Implemented MLPs, embeddings, self-attention, and Transformer blocks in PyTorch/NumPy.
- Trained a 7M-parameter character-level GPT (“Frosty”) to generate plausible verses in the style of Robert Frost.
- Fully reproducible with clear walkthroughs and annotated notebooks.\

📈 **Sample output from *Frosty***:
  ```
  To learned me there with other they forget—in verning. 
  You see and not blown?’ have to losen. 
  
  God their race are that of those provals across the brook 
  Be there blacked to himself on a man, 
  But almost There thoughow hear were and fool. 
  ```

<!--
A walkthrough of Andrej Karpathy’s Zero to Hero YouTube series. Includes:
- A build of [micrograd](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode-1/micrograd): experiments on custom activations, and attempts at understanding neuron activations. Exploratory/blog-style notes and diagrams (with more to come!)
- [makemore](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode_2), a character-level language model inspired by Karpathy’s series. So far, we've implemented a bigram model that predicts the next character from the previous one, trained on the names dataset. Next, we are extending this to a flexible context window model that utilizes multiple preceding characters. Along the way, we are incorporating techniques from later episodes—like improved optimization strategies and training intuition. For readers interested in interpretability and training dynamics (e.g., why normalization matters), see also the interpreting_mnist repo below.
- [Generative Pretrained Transfomer (GPT)](https://github.com/eriktholmes/zero_to_hero_course/tree/main/gpt): We build up slowly from a simple bigram model-as in makemore-to a samll decoder only transformer trained on a CPU, and eventually end by scaling up the models parameters and running on a T4 GPU. We train the model on the works of Robert Frost: (here's one somewhat structured but nonsensical output... it is a small character level model at the end of the day!)\
    - [Here](https://github.com/eriktholmes/educational_notebooks/blob/main/Transformer_outline.ipynb) is a short(ish) blurb on the transformer architecture that I wrote to accompany this project... I hope to clean it up in the near future and add some relevant visualizations!
  > ```
  > ONENT 
  >
  >
  > And flower what checks a smile darled out end 
  > dows for a farmica cellar to fice. 
  >
  > The fame needn’t know that’s have left. 
  >
  >
  > Neither expered. His earn one. 
  > 
  >
  > [ 275 ]
  > ```

    - For comparison purpsoses I also finetuned a [tinyllama](https://huggingface.co/TinyLlama/TinyLlama-1.1B-intermediate-step-1431k-3T) model by feeding it the Robert Frost dataset. Here is one of the poems the model generated:
  > ```
  > THE RUTHLESS STAR  
  >
  > You have to admit, when I was a boy, I had a star.  
  > 
  > Sitting on its own high, high in the sky.
  >
  > What a strange thing to do, to have a star,  
  >
  > When I was only a little boy.
  >
  > But I was a boy then, and I knew I was a boy.  
  >
  > And I knew this star, with its own little sky,  
  >
  > And I knew it had to do what it wanted to do.  
  >
  > And I knew this star, with its own little sky,  
  >
  > And I knew it had to do what it wanted to do.  
  >
  > But not to me, I'm sure, was there any special reason.  
  >
  > I only know I was astonished.  
  >
  > And I was very lonely. There sat my star.  
  >
  > And there was no one to say a word to.  
  >
  > [No 199] 
  > ```
-->

---

## [```ai_sandbox```](https://github.com/eriktholmes/ai_sandbox) 
An informal space for ML/AI experimentation — currently focused on reinforcement learning and game-playing agents.

- **Current focus**: AlphaZero-lite implementations for small board games.
    - Built game environments for Tic Tac Toe and Connect Four:
        > <img width="120" height="120" alt="Screenshot 2025-08-07 at 2 49 44 PM" src="https://github.com/user-attachments/assets/aabf5c0c-5cae-46ea-ad9f-d8fdbda360ce" />    <img width="140" height="120" alt="Screenshot 2025-08-06 at 12 44 18 PM" src="https://github.com/user-attachments/assets/5db680f6-fa78-4e74-8601-c4f153d208ce" />
    - Implemented basic Monte Carlo Tree Search (MCTS) for Tic Tac Toe
    - Ran baseline simulations to benchmark simple strategies:
        - Random vs. Random
        - Random vs. Greedy
        - Random vs. MCTS
    - Next steps: integrate value networks, train self-play agents, and add an interactive environment to play against them.


<!--
### [`Math_things`](https://github.com/eriktholmes/math_things)
A catch-all for math-related code, currently focused on:
- Computational experiments related to unit lattices in number fields
- Visualization of rank 2 shapes within the [fundamental domain](/Math_things/unit_shapes/FD_domain.png)
- Ongoing research on lattices and questions of distribution
- Ultimately, I am excited about a possible application of lattice shapes to log terms in Malle's conjecture (which is roughly about the asymptotics of specialized counting functions) and hope to have some code related to that at some point...?
-->
<br> 

## 🪚 Some current/recent work:
- 🔧 [micrograd](https://github.com/eriktholmes/zero_to_hero_course/tree/main/micrograd), [makemore](https://github.com/eriktholmes/zero_to_hero_course/tree/main/makemore), [gpt_mini](https://github.com/eriktholmes/zero_to_hero_course/tree/main/gpt): foundational deep learning models, built for hands-on learning
- 🔬 [interpreting_mnist](https://github.com/eriktholmes/interpreting_mnist/tree/main/MLP): exploratory repo on internal neuron behavior (activation drift, normalization effects, etc.)
- 🧠 [mlp_explained_pytorch](https://github.com/eriktholmes/educational_notebooks/blob/main/mlp_explained_pytorch.ipynb): breakdown of an MLP in PyTorch, inspired by the micrograd build
- 🎲 [ai_sandbox](https://github.com/eriktholmes/ai_sandbox): experimental repo, currently looking at reinforcement learning environments and AlphaZero-style agents
- 🔣 [Number theory research](https://erikholmesmath.com/research.htm): ongoing collaborations on lattices in number theory, and in how their geometry varies within *natural* families. 

<br> 

## About this github:
Most repos here include small from-scratch builds, visualizations, and interpretability experiments. I aim for readable, testable, and educational work — both for myself and others. More about my approach [here](https://github.com/eriktholmes/eriktholmes/blob/main/learning_approach.md).


<br>
<br> 

## 🔗 Contact & More
- 📫 eriktholmes@gmail.com
- 🌐 [erikholmesmath.com](https://erikholmesmath.com)


<!---
eriktholmes/eriktholmes is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
