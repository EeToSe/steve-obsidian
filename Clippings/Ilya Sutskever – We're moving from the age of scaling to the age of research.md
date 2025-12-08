---
categories:
  - "[[Podcast episodes]]"
topics:
  - "[[AI]]"
author:
  - "[[Dwarkesh Patel]]"
source: https://www.dwarkesh.com/p/ilya-sutskever-2
published: 2025-11-26
created: 2025-12-04
guests:
  - "[[Ilya Sutskever]]"
show:
  - "[[Dwarkesh Podcast]]"
tags:
  - todo/1
---
## **The Return to the Age of Research (21:16):**

- **Shifting Focus from Scaling to Research:** While the period from 2020-2025 was dominated by scaling (pre-training with massive data and compute), Ilya suggests we are returning to an "age of research." This means the focus will shift from simply scaling existing recipes to discovering new fundamental machine learning principles.
- **Beyond Pre-training:** Pre-training, while a breakthrough, will eventually run out of data (21:02). Future progress will likely come from "souped-up pre-training," different recipes, or entirely new approaches like more efficient RL or other training paradigms (21:07-21:13).
- **Ideas Over Pure Compute:** While large compute is helpful for building the _absolute best_ systems and differentiating within the same paradigm (39:26-39:39), Ilya argues that sufficient compute, not necessarily the _absolute largest_, is needed to prove new ideas in research (39:13-39:18, 41:42-42:01). The bottleneck is shifting back to generating novel ideas rather than just execution at scale (37:37-37:47).

## **The Crux of Generalization (25:00):**

- **AI Models Generalize Worse than Humans:** A fundamental challenge is that current AI models generalize "dramatically worse than people" (25:00-25:06). This disconnect between high performance on evaluations and real-world utility needs to be addressed (4:46-4:52).
- **Sample Efficiency and Robustness:** Humans exhibit far greater sample efficiency (learning from less data) and robustness compared to models (25:20-25:24, 30:06-30:09). This suggests that humans possess some "fundamental thing" beyond just complicated priors that makes them good at learning (28:21-28:27).
- **The "It Factor" (7:50):** The analogy of two students in competitive programming highlights this: one who practices 10,000 hours and another who does well with only 100 hours of practice. The latter possesses an "it factor" or better generalization that models currently lack (6:09-7:53).

## **The Role of Emotions and Value Functions (9:39):**

- **Emotions as Value Functions:** Ilya discusses the human analogy of a person with damaged emotional processing becoming unable to make decisions. He suggests emotions serve as a "value function" that guides decision-making and provides an immediate reward signal, even in long-term tasks.
	![[IQ-bell-curve-meme.png]]
	- low-IQ folks trust their instincts outright,
	- midwits overcomplicate things with "correct" but not necessarily true reasoning.
	- high-IQ ones can articulate and refine those same instincts.
It's a fun analogy here, because a well-trained value function could be seen as that "articulated instinct" for an AI—immediate, reliable signals that smart systems learn to rely on, bypassing naive trial-and-error.

## **Practical Tools and Approaches:**

- **Leveraging AI for Research:** The podcast host describes using **Gemini 3** to brainstorm, find connections between ideas, generate code for experiments, and analyze results, highlighting its utility for accelerating research and gaining intuitive understanding (33:51-35:34).
- **Data Labeling for Specific Needs:** **Labelbox** is mentioned as a tool that helped the host create custom data for transcription that met specific, nuanced requirements (e.g., reworded to read like essays, not just verbatim), emphasizing the importance of tailored data for fine-tuning and specialized AI tasks (description).
- **AI for Risk Management:** **Sardine** is presented as an AI risk management platform that uses various signals and AI agents to automate fraud investigations, showing how AI can be applied to scale defenses against AI-powered attacks (description).

## **Strategic Considerations for Founders:**

- **Focus on Research First:** SSI's current strategy is to focus solely on research, with the belief that a path to monetization will reveal itself later (42:52-42:59).
- **Unpacking Funding:** While other companies might raise more, a significant portion of their funds goes to inference, large staff, and product-related features, making the actual research budget difference smaller (41:08-41:41).
- **Potential for Strategic Shifts:** The "straight-shot to superintelligence" plan may change if timelines prove longer or if there's significant value in having powerful AI impacting the world sooner (43:21-43:41).