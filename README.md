
<h1 align="center"> Erik Holmes </h1>
<h3 align="center">   Mathematics | Machine Learning | Research  </h3>

<br>

  | <sub>⚠️ Disclaimer: This GitHub is part learning journal/blog, part experimental sandbox — evolving as I work through various projects. It's a bit nerdy, occasionally verbose, and sometimes a little chaotic — but the goal is to build a rigorous foundation in maachine learning with a focus on interpretability and alignment.</sub>| 
  | --------- | 
<br>

# About Me
I’m a postdoctoral researcher at the University of Toronto, specializing in number theory and arithmetic statistics. I'm now pivoting into machine learning, motivated by the opportunity to apply rigorous thinking to high-impact, real-world challenges.


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



## 🎯 Goals

> Building toward an interpretability/safety-focused ML research or engineering role by **August 2025**.

### 🔍 Current Focus (Summer 2025)
- **Rebuild foundational ML models from scratch**: micrograd, makemore, and a minimal GPT — to deeply understand core architectures, training dynamics, and attention mechanisms
- **Probe internals of trained vision models**: analyze MLP/CNN classifiers on MNIST using neuron selectivity, ablation, activation drift, and PCA/UMAP-based subspace analysis
- **Explore toy reinforcement learning agents**: build AlphaZero-lite implementations (e.g., Connect Four) with Monte Carlo Tree Search and policy/value networks
- **Use interpretability tooling on Transformers**: focus on TransformerLens
- **Investigate fine-tuning effects on representation space**: examine how supervised or preference-based fine-tuning shifts neuron behavior, attention patterns, and decision boundaries

### 🔭 Long-Term
- Contribute to safe, interpretable AI systems
- Apply math/ML hybrid skills to real-world problems
- Collaborate on research that bridges theory and applied ML


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
This repo explores the internal workings of image classifiers - to break apart/intervene in the black box and try to interpret the inner workings. The goal is to build and document real interpretability tools — starting from first principles and scaling up.

The project is structured as two parallel tracks (for now): one using a basic MLP, the other (in progress) extending to a CNN. Each track is presented through annotated notebooks with exploratory commentary, code, and visualizations. The final goal is to distill these findings into a blog post/write-up.

### Part 1: [`MLP`](https://github.com/eriktholmes/interpreting_mnist/tree/main/MLP):
We dedicate three notebooks to this experiment: throughout our model is a 2 layer MLP (32 -> 16 neuron hidden layers). We use SGD and fixed learning rate over 20 epochs.

All analysis is on MNIST. The track is organized into three notebooks:


- **Notebook 1: (unnormalized baseline)**
  >
  > Some experiments include:
  > - track neuron activations across epochs: manually in this notebook, then with hooks in notebook 2.
  > - Class-based activation statistics to identify class-specific or feature-detecting neurons
  > - Activation drift analysis, showing how selectivity changes over time
  > - Dimensionality reduction (PCA, t-SNE, UMAP) applied to the final hidden layer
 
- **Notebook 2**: (further unnormalized investigations)
  > We go deeper into interpretability and causality:
  > - Compute top-activating neurons per class — many show cross-class activation (shared features)
  > - Introduce selectivity scores, comparing mean activation on a class vs. others
  > - Perform causal interventions:
  >     - Neuron ablation: zeroing out individual neurons
  >     - Neuron scaling: multiplying activation values
  > - Apply dimensionality reduction techniques on highly selective subspaces:
  >     - take the top-$k$ neurons that are highly selective on a fixed class and apply UMAP on the $k$-dimensional subspace spanned by these neurons.
  > We see:
  > - Bottleneck neurons that control accuracy for specific classes — ablating them drops class accuracy to ~0%; scaling increases it monotonically
  > - A confusion matrix showing clear misclassifications between structurally similar digits (e.g., 4, 7, 9)
  > - Some class clustering (UMAP) on selective subspaces but its fairly noisy.


- **Notebook 3**: with normalization and dropout (currently being cleaned up)
  > We repeat the same experiment setup with:
  > - Normalized inputs
  > - Layer normalization
  > - Dropout (to prevent overfitting)
  > We observe:
  > - Faster training: matches baseline accuracy in a quarter to half of the epochs
  > - Better generalization: reduced overfitting and more stable neuron behavior
  > - UMAP on top selective neurons shows clearer clustering with possible submanifold shadows — the data forms curves or paths in the latent space, suggesting underlying geometric structure --> We are investigating this further:


- **Some visualizations:**
  > |     |   Activation drift   |  Neuron scaling | Confusion Matrix | UMAP class selective subspace |
  > | --- | :---------: | :-------: |:-------: | :-------: |
  > |Non-normalized| <img width="736" height="570" alt="Screenshot 2025-07-30 at 3 16 32 PM" src="https://github.com/user-attachments/assets/b35bbe13-b30d-4d74-8ebc-29d745cad1d0" />|<img width="871" alt="Screenshot 2025-07-05 at 5 46 51 PM" src="https://github.com/user-attachments/assets/71019267-ea5b-4088-98ad-3695376ad478" />|<img width="521" alt="Screenshot 2025-07-04 at 2 12 04 PM" src="https://github.com/user-attachments/assets/cf03f4cb-2529-4304-8b91-89fc052f53d2" />|<img width="927" height="671" alt="Screenshot 2025-08-06 at 11 46 30 AM" src="https://github.com/user-attachments/assets/cd13d09b-87d8-4882-afa6-75881d6be62d" />|
  > |Normalized|<img width="743" height="562" alt="Screenshot 2025-08-06 at 11 56 54 AM" src="https://github.com/user-attachments/assets/d4d00adb-16fb-4640-b0e7-b72382ed8dda" />|<img width="869" height="660" alt="Screenshot 2025-08-06 at 11 39 05 AM" src="https://github.com/user-attachments/assets/8b857c5d-a2e7-4ab3-9fdb-d60a60bee24d" />|<img width="535" height="544" alt="Screenshot 2025-08-06 at 11 39 24 AM" src="https://github.com/user-attachments/assets/7a857f8f-58a5-413f-9ef3-1f11343a86da" />|<img width="883" height="674" alt="Screenshot 2025-08-06 at 11 41 52 AM" src="https://github.com/user-attachments/assets/98bc797e-9976-4de1-ac0c-e09687cf8103" />|


-  I have numerous questions/experiments in mind at this point: from selectively based prune and its affect on model interpretability, to selectively based subspace analysis, and ultimately to compare the MLP experiments with CNN vs Transformer architechures. In any case, there will be more to come!


---


## [`Zero-to-hero-course`](https://github.com/eriktholmes/Zero-to-hero-course)
A walkthrough of Andrej Karpathy’s Zero to Hero YouTube series. Includes:
- A build of [micrograd](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode-1/micrograd): experiments on custom activations, and attempts at understanding neuron activations. Exploratory/blog-style notes and diagrams (with more to come!)
- [makemore](https://github.com/eriktholmes/Zero-to-hero-course/tree/main/episode_2), a character-level language model inspired by Karpathy’s series. So far, we've implemented a bigram model that predicts the next character from the previous one, trained on the names dataset. Next, we are extending this to a flexible context window model that utilizes multiple preceding characters. Along the way, we are incorporating techniques from later episodes—like improved optimization strategies and training intuition. For readers interested in interpretability and training dynamics (e.g., why normalization matters), see also the interpreting_mnist repo below.
- [Generative Pretrained Transfomer (GPT)](https://github.com/eriktholmes/zero_to_hero_course/tree/main/gpt): We build up slowly from a simple bigram model-as in makemore-to a samll decoder only transformer trained on a CPU, and eventually end by scaling up the models parameters and running on a T4 GPU. We train the model on the works of Robert Frost: (here's one somewhat structured but nonsensical output... it is a small character level model at the end of the day!)
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

For comparison purpsoses I also finetuned a tinyllama model by feeding it the Robert Frost poems. Here is one of the resulting poems:
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


---

## [```ai_sandbox```](https://github.com/eriktholmes/ai_sandbox) 
An informal space for ML/AI experimentation — currently focused on reinforcement learning and game-playing agents.

- Currently working on AlphaZero (lite). So far we have:
    - Built custom environments for Tic Tac Toe and Connect Four
        > <img width="140" height="120" alt="Screenshot 2025-08-06 at 12 44 18 PM" src="https://github.com/user-attachments/assets/5db680f6-fa78-4e74-8601-c4f153d208ce" />
    - Implemented basic Monte Carlo Tree Search (MCTS) for Tic Tac Toe
    - Ran baseline simulations to benchmark simple strategies:
        - Random vs. Random
        - Random vs. Greedy
        - Random vs. MCTS
    - Coming soon:
        - integrating value networks
        - training self-play agents
        - and (hopefully) a game environment to play against the Alphazero agents in each game.
  


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
<br> 

## 🔗 Contact & More
- 📫 eriktholmes@gmail.com
- 🌐 [erikholmesmath.com](https://erikholmesmath.com)


<!---
eriktholmes/eriktholmes is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
