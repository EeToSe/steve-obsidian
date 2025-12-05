---
categories:
  - "[[Podcast episodes]]"
topics:
  - "[[LLM]]"
source: https://www.dwarkesh.com/p/andrej-karpathy
published: 2025-10-18
created: 2025-10-26
tags:
  - clippings
show:
  - "[[Dwarkesh Podcast]]"
guests:
  - "[[Andrej Karpathy]]"
host:
  - "[[Dwarkesh Patel]]"
status: todo
---
## Breakthrough moments brief review
- training neural nets per-tasks
- trying the first round of agents 
- LLMs and seeking the representation power of the neural networks

The period around 2013-2017, when we were trying to build agents using reinforcement learning (RL) on tasks like Atari games or even web pages (like the Universe project at OpenAI). The point is that we were trying to get the "full thing"—a complete, acting agent—**too early**. 

1. **Wrong Order (What we tried):** `Random Agent` $\rightarrow$ `RL on hard task` $\rightarrow$ `(FAIL: sparse reward)`
2. **Right Order (What we do now):** `Pre-train LLM (builds representation)` $\rightarrow$ `Use LLM as agent's brain` $\rightarrow$ `Fine-tune/RL on hard task` $\rightarrow$ `(SUCCESS: agent understands the task)`

## [Steelman](https://en.wikipedia.org/wiki/Straw_man#Steelmanning) the [Sutton perspective](https://www.dwarkesh.com/p/richard-sutton)
Sutton, the author of the post, is not so sure that LLMs are "bitter lesson pilled" at all. They are trained on giant datasets of fundamentally human data, which is both 1) human generated and 2) finite. What do you do when you run out? How do you prevent a human bias?

## **Andrej**'s [write-up about that podcast](https://x.com/karpathy/status/1973435013875314729)
Frontier LLMs are now highly complex artifacts with a lot of humanness involved at all the stages 
- the foundation (the pretraining data) is all human text, 
- the finetuning data is human and curated, 
- the reinforcement learning environment mixture is tuned by human engineers. 

We do not in fact have an actual, single, clean, actually bitter lesson pilled, "turn the crank" algorithm that you could unleash upon the world and see it learn automatically from experience alone.

The "ghost" or "spirit" analogy is my way of explaining _why_ LLMs are different from animals and why trying to build them like animals (Sutton's perspective) might be the wrong analogy for what we're actually doing.
- Animals come with a huge amount of "hardware" that's "baked in" by **evolution**.
- We are taking the entire "digital exhaust" of humanity and this creates a different kind of intelligence:
	- **Ethereal & Digital:** It's a "ghost" because it's a "spirit entity" that is fully digital. It doesn't have a body, it doesn't interact with the physical world, and it hasn't learned from physical survival.
	- **An Echo of Humanity:** An LLM is a _statistical echo_ of all the humans who created its training data. It's a "distillation" of our collective culture, knowledge, and biases.
	- **A "Human Artifact":** It's an artifact _of_ humanity, not a new _animal_ created _by_ nature.

This is why I call pre-training our **"crappy evolution."** We are doing training by imitation of humans and the data that they’ve put on the Internet. This "ghost" is the cognitive core, the power of representation, that we were missing before. If you imagine a space of intelligences, we’re starting off at a different point almost. We’re not really building animals. But it’s also possible to make them a bit more animal-like over time, and I think we should be doing that.

## Takeaways for phd
- **Understand the Current State of Agents:** The speaker believes that while early agents like Claude and Codex are impressive, there's **a decade of work** (1:21 - 1:25) to be done before they can act like a full employee or intern. The current bottlenecks include a lack of intelligence, multimodality, computer use capabilities, continual learning, and general cognitive deficits (2:13 - 2:31). This suggests that your research should focus on these areas of improvement.
- **Prioritize Building and Coding over Theory/Writing:** The speaker strongly advises against just writing blog posts or slides. Instead, he emphasizes the importance of **building the code, arranging it, and getting it to work** (30:27 - 30:31). This hands-on approach is crucial for uncovering what you truly don't understand, leading to deeper knowledge (30:00 - 30:13).
- **Hands-on Learning is Key:** When learning from existing repositories like nanochat, the speaker suggests putting the code on one monitor and **building it from scratch yourself** on another, without copying and pasting (29:06 - 29:17). This process forces you to confront your gaps in understanding.
- **Be Skeptical of AI Agent Capabilities in Complex, Unique Tasks:** While coding models are good for boilerplate or frequently occurring code (31:40 - 31:53), they were of little help in building a unique repository like nanochat (31:58 - 32:08). This is because models often misunderstand non-typical code and rely too much on existing internet patterns (32:16 - 32:27). For complex, intellectually intense projects, the human "architect" role is still essential (31:13 - 31:17).
- **Focus on the "Cognitive Core" of Intelligence:** The speaker suggests that current LLMs pick up both knowledge and intelligence during pre-training. He believes that for future agents, we need to **figure out ways to remove some of the "knowledge"** and retain the "cognitive core" that contains algorithms, magic of intelligence, problem-solving, and strategies (14:22 - 14:38). This implies exploring methods that can strip away reliance on rote knowledge and enhance adaptive problem-solving.
- **Distillation for Continual Learning is a Missing Piece:** Analogizing to human sleep (He explains that when humans are awake, they build up a context window of daily events. However, during sleep, a "magical" process occurs where this temporary context window doesn't simply disappear but is **distilled into the weights of the brain**), the speaker points out that LLMs currently lack a "distillation phase" (23:30 - 23:38) where they analyze what happened, think through it, and integrate new information into their weights for long-term memory. This "continual learning" capability, especially for very long contexts, is seen as currently absent and a significant area for research (23:35 - 24:22).
- **Evolution vs. Current AI Training:** Be cautious about making direct analogies between animal learning/evolution and AI training. The speaker argues that animals come with a **huge amount of built-in hardware from evolution** (8:48 - 9:00), and much of what looks like learning in animals is actually brain maturation, with very little "reinforcement learning" for intelligence tasks (10:25 - 10:40). Our current AI builds "ghosts" by imitating human data, not evolving "animals" (9:23 - 9:45). Pre-training is described as a "crappy evolution" (12:50 - 12:56) – a practical way to get a starting point for models given our current technology.
- **Future Architecture: More Sparse and Larger:** In 10 years, the speaker expects AI to still involve **giant neural networks trained with gradient descent** (27:01 - 27:04), but with more modified attention and possibly sparser architectures (24:52 - 24:57), converging on similar cognitive architectures that evolution came up with (24:42 - 24:49). Progress will likely come from simultaneous improvements across data, hardware, software, and algorithms (26:30 - 26:46).