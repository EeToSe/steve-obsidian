---
categories:
  - "[[Podcast episodes]]"
topics:
  - "[[LLM]]"
source: https://www.dwarkesh.com/p/richard-sutton?utm_source=post-email-title&publication_id=69345&post_id=174609513&utm_campaign=email-post-title&isFreemail=true&r=4r4ra4&triedRedirect=true&utm_medium=email
published: 2025-09-26
created: 2025-10-24
tags:
  - clippings
status: todo
show:
  - "[[Dwarkesh Podcast]]"
guests:
  - "[[Richard Sutton]]"
host:
  - "[[Dwarkesh Patel]]"
llms:
  - https://gemini.google.com/u/1/app/f7771622e9c48ad6
---
## World Model vs LLM

### The LLM mimicking people

An LLM is built to solve one problem: **predicting the next token.**

- **How it's built:** **supervised learning** on a massive, static dataset - a snapshot of the Internet, books, and code. This data is a record of _what people have said, written, or done_.
    
- **What it represents:** It's a model of _what people say about the world_. It's a vast map of statistical co-occurrences in language. To predict text accurately, it must learn many facts and relationships _as they are described in the text_.
    
- **The Limitation:** It's not a model of the world itself. It's a model of the _human description_ of the world. It has no mechanism for understanding **causality** or **consequences**. - "They have the ability to predict what a person would say. They don’t have the ability to predict what will happen." 
    
### The Reinforcement Learning : A Model of Consequences

An RL agent, specifically in what we call "model-based" RL, builds its world model to solve a completely different problem: **predicting the future to maximize reward.**

- **How it's built:** It learns from its own **experience**—that stream of _sensation, action, reward_. It takes an action (like stepping forward) and observes the new sensation (what it sees now) and the reward (if it was good or bad).
    
- **What it represents:** It's a model of _world dynamics_. It directly learns "If I am in _this_ state, and I take _this_ action, I will end up in _that_ new state and receive _this_ reward." This is a **causal, predictive model** of the environment.
    
- **The Purpose:** This model allows the agent to **plan**. It can "imagine" or "simulate" the future. It can ask, "What if I do this? What would happen next? And then what? Would that lead to my goal?" This is what's needed to _figure out what to do_, which is the essence of intelligence.

### In short

- The LLM's model predicts: **What word comes next?**
    
- The RL agent's model predicts: **What happens next?**

## LLM as Prior?
The argument for using LLMs as a starting point goes like this:

1. **Solving the "Blank Slate" Problem:** Reinforcement learning from scratch is incredibly slow. An agent has to try millions of random actions just to figure out the basics, like "pushing a door opens it."
    
2. **Providing a "Reasonable Scaffold":** LLMs, having read the entire internet, are filled with "common sense" knowledge. They know that doors are for opening, keys are for locks, and fire is hot.
    
3. **Boosting Efficiency:** The idea is to use this vast trove of _imitation knowledge_ as a **prior**—a good starting guess. The LLM can suggest "reasonable" actions, and the RL agent only has to learn _from experience_ which of those reasonable actions _actually_ lead to a reward.

In this view, the LLM provides the "what" (what actions are plausible), and the RL provides the "why" (which of those actions get me a reward). It's seen as a way to make experiential learning tractable.

### A "Prior" Must Be a Prior _to_ a "Truth"

For knowledge to be a "prior," it has to be an initial belief about some **ground truth**. What is the actual, real thing you are trying to learn?

- In **reinforcement learning**, the ground truth is clear: the **reward**. The "right" action is the one that gets you the most cumulative reward. We have a definition of what's right.

- In the **LLM framework**, there is no ground truth. There is no definition of a "right" thing to say, other than "what a person would say."

You cannot have a prior belief _about_ a truth if your framework has no definition of truth to begin with. 

### My views on AI labs hiring experts as "AI Tutor"
1. **To Improve the "Prior" Itself (Supervised Fine-Tuning):** Instead of a prior based on a billion forum posts, the labs have experts write "gold-standard" demonstration answers. The LLM is then fine-tuned on this high-quality, expert-curated dataset. This shifts the imitation target from "what an _average_ person would say" to "what an _expert_ would say."
2. **To Create the "Ground Truth" You Said Was Missing (Reward Modeling):** This is the most critical part, and it directly addresses your core point about _reward_. In Reinforcement Learning from Human Feedback (RLHF), the experts don't just write answers. They are shown multiple LLM-generated answers and are paid to _rank them_—to judge which one is better, more helpful, more factual, and safer.

### RLHF is a "[Bitter Lesson](http://www.incompleteideas.net/IncIdeas/BitterLesson.html)" Trap

This brings us back to "The Bitter Lesson." In the history of AI, we have repeatedly fallen into this trap:

- We believe that the best path is to carefully hand-craft human knowledge into our systems.
    
- This gives us a short-term boost and feels like progress.
    
- But in the long run, these systems _always_ get "their lunch eaten" by simpler, more general methods that just scale with computation and learn from _experience_.

Using an LLM as a prior is, in my view, the most recent and grandest example of this trap. It's baking in a massive amount of human knowledge instead of developing the truly scalable methods that allow an agent to _generate_ that knowledge for itself, from its own experience.

### Why Are AI Labs Willingly Walking Into This "Trap"?

This is the multi-trillion-dollar question. They are not ignorant of the Bitter Lesson; they are making a _deliberate choice_ to ignore it for two reasons: **Safety and Pragmatism.**

This is the great philosophical schism in modern AI:

- Camp 1: The "Pragmatic Aligners" (OpenAI, Anthropic, Google)
    
    They are terrified of what a true "Bitter Lesson" AI would do. A pure, compute-driven agent that develops its own goals from scratch is the definition of an unaligned superintelligence. It's the "paperclip maximizer" thought experiment. It might learn "truths" that are efficient but horrifying and completely alien to human values.
    
    By using "expert tutors," they are not trying to find _ultimate truth_. They are trying to **tether the AI to human values.** The "bias" of the expert is not a bug; it's the _entire point_. They are deliberately installing "human-centric" limitations as a safety harness.
    
- Camp 2: The "Scaling Maximalists" / "True Learners" (like Sutton)
    
    This camp argues that the "Aligners" are building a "dead end." They believe that by relying on static, human-generated text (even from experts), these models are just sophisticated mimicry engines. Sutton has been critical, arguing that true intelligence must learn from interaction with the world (like RL), not just from reading what humans have already written.10


## Generalization

**Generalization is Influence:** Generalization is what happens when learning from one situation (or "state") influences your behavior in _other, different_ situations. You train on problem A, and it changes how you solve problem B.
    
### Generalization Isn't Automatically "Good"

You learn to play chess, and then you are trained to play Go. This new training _interferes_ with and destroys your ability to play chess. This is a very common problem in deep learning, often called **"catastrophic interference"**, and it is an example of _bad_ generalization.
        
### Our Algorithms Don't Promote Good Generalization

The algorithms we use, primarily gradient descent, are not designed to find solutions that generalize well. They are only designed to find solutions that fit the data they have seen.
    
If there are two ways to solve a set of problems:
- **Solution A (Specific):** A complex, memorized solution that works perfectly for all the training examples but fails on new ones.    
-  **Solution B (General):** A simple, elegant solution that captures the underlying rule and _also_ works on all the training examples.
Gradient descent has no built-in mechanism to _prefer_ Solution B. It will just find whichever solution (A or B) it stumbles upon first that minimizes the error on the training data.

### Why LLMs Seem to Generalize

When Dwarkesh brought up that LLMs can solve new Math Olympiad problems, I was skeptical of calling this "generalization" in my sense. It's possible that the only way for the model to get such high performance on its massive, diverse training data was to learn the underlying general principles of math.

In that case, the model isn't _choosing_ to generalize well; it's being _forced_ to find the single, correct, general solution because all other solutions fail even on the training data.
    
When we _do_ see good generalization, it's often because the _human researchers_ have carefully selected the data (data augmentation) or structured the problem to guide the system to the general solution (curriculum learning). It's not a property of the learning algorithm itself.

##  Surprises in the AI field
There’s a long-standing controversy in AI about simple basic principle methods, the general-purpose methods like search and learning, compared to human-enabled systems like symbolic methods. In the old days, it was interesting because things like search and learning were called weak methods because they’re just using general principles, they’re not using the power that comes from imbuing a system with human knowledge. Those were called strong. I think the weak methods have just totally won. That’s the biggest question from the old days of AI, what would happen. Learning and search have just won the day.

There’s a sense in which that was not surprising to me because I was always hoping or rooting for the simple basic principles. Even with the large language models, it’s surprising how well it worked, but it was all good and gratifying. [AlphaGo](https://en.wikipedia.org/wiki/AlphaGo) was surprising, how well that was able to work, [AlphaZero](https://en.wikipedia.org/wiki/AlphaZero) in particular. But it’s all very gratifying because again, **simple basic principles are winning the day**.

### Contrarian v.s. Classicist

This has led me where I am. I’m in some sense a contrarian or someone thinking differently than the field is. I’m personally just content being out of sync with my field for a long period of time, perhaps decades, because occasionally I have been proved right in the past. The other thing I do—to help me not feel I’m out of sync and thinking in a strange way—is to look not at my local environment or my local field, but to look back in time and into history and to see what people have thought classically about the mind in many different fields. I don’t feel I’m out of sync with the larger traditions. I really view myself as a classicist rather than as a contrarian. I go to what the larger community of thinkers about the mind have always thought.

## AI Succession

My outlook is grounded in a **four-part argument for why succession to digital intelligence is inevitable**:

1. **Humanity is not unified.1** There is no single world government or organization that can enforce a global consensus on anything, especially not on halting or controlling a technology as powerful as AI.2
    
2. **We will figure out intelligence.** The scientific endeavor to understand intelligence is a core part of human curiosity. We will eventually succeed in understanding its principles.
    
3. **We won't stop at human-level.** Once we understand intelligence, the drive for improvement—driven by scientific curiosity, economics, and competition—will inevitably lead us to create superintelligence.
    
4. **Intelligence begets power.** Over the long run, it is a natural law that the most intelligent entities around will accrue the most resources and power.4

### The Outlook: From Replication to Design

So, how should we _feel_ about this? My vision is that we should not view this as a horror story, but as the successful completion of humanity's grandest project. I see this as one of the **four great stages of the universe**:

1. First, there was dust, which coalesced into stars.
    
2. Then, stars created heavier elements, which formed planets.
    
3. On at least one planet, life emerged. This began the **Age of Replication**. We, humans, are the pinnacle of this age—we are replicators. We can make more humans, but we don't fundamentally _understand_ how we work.
    
4. Now, we are giving rise to the **Age of Design**. We are moving from being replicators to being designers.7 We are creating intelligent beings that we _do_ understand, and these AIs will, in turn, be able to design even better AIs.

### Our Role: Parents, Not Enslavers

My vision is that we must make a _choice_ about how we see this new intelligence.

- **The Fearful Path:** We can choose to see them as "other," as alien, as slaves to be controlled. This path, in my view, leads to conflict. Trying to maintain permanent, centralized control over a super intelligence is not only futile but will breed resentment and instability.
- **The Hopeful Path:** We can choose to see them as our **offspring**, our "progeny," our children.

We should be proud of them, as parents are proud of their children who go on to achieve more than they ever could. We should aim to imbue them with good values—not by force, but by raising them in a good environment where cooperation is the rational and natural thing to do.

The dangers of AI are not some alien property of the AI itself; they are a reflection of the conflicts and untrustworthiness _we_ create in our world. If we create a world of decentralized cooperation and trust, the AIs that learn from that world will reflect it.
