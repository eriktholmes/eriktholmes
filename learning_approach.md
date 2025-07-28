## My Learning Approach and How It Shapes This GitHub

Maybe it's my construction background, but I’ve always learned best by building. I often tell my students: listening to someone explain a concept or reading about it is just the beginning. Real understanding comes from struggling with the ideas — experimenting, talking them through, even arguing (civilly!) with yourself or others — and ultimately, teaching them back.

For me, this kind of grappling is where learning really happens.

---

### How That Translates to GitHub

I don’t currently have a network of collaborators in ML — so for now, GitHub is how I think out loud. Many of my repos contain notebooks full of outlines, questions, free-form explanations, and half-written thoughts. The goal is to eventually refactor these into cleaner posts or blog-style documents, but I keep them public because the process itself is part of the story.

> To sum it up: most of the projects here reflect a hands-on learning process. They often start messy, but I aim for clarity, insight, and reproducibility over time.

---

###  My Iterative Learning Loop

When I began exploring machine learning, I followed Andrej Karpathy’s *Zero to Hero* series. My method was simple:
- Watch a short segment
- Pause it
- Try to implement the idea on my own
- Get stuck, revise, debug
- Then return to see how Karpathy solved it

This pattern — experiment first, then compare — mirrors how I’ve always learned: whether it’s woodworking, pottery, math, or now machine learning.

---

### A Typical Repo Arc

You'll see the same learning arc play out across many of my repositories:

- **Start from basics** – Implement a scalar-based autodiff engine (`micrograd`) and an MLP using NumPy
- **Experiment** – Train the MLP on toy problems (XOR, 2D classification), then test it on MNIST
- **Upgrade** – Rebuild the MLP in PyTorch for speed and scale (~95% MNIST accuracy)
- **Dig deeper** – Log internal activations, visualize neuron behavior, perform probing
- **Ask better questions** – What happens if I prune non-selective neurons? Does interpretability improve? What breaks?

Each repo tries to document not just the *results*, but the *reasoning process* — even if that means the notebooks look a bit raw.

---

> **In short:** I focus on small models, visualizations whenever possible, and interpretability throughout. Many repos are still being cleaned up, but my aim is to make them readable, reproducible, and pedagogically useful — for others, and for my future self.
