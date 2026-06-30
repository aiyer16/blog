---
title: Are We Delegating the Mechanics, or the Mastery?
date: 2026-06-28
draft: false
tags:
  - artificial-intelligence
  - productivity
source:
---
I recently read an interesting piece by Fran Soto on how to use AI effectively. You can read the original article [here](https://strategizeyourcareer.com/p/one-config-bug-changed-my-ai-workflow). 

Fran's central thesis is that engineers should transition to an "executive" role, delegating mechanical tasks, like code investigation and syntax checking, to AI, while reserving decisions regarding architecture, product risk, and system tradeoffs for human judgement. To drive this home, he uses an example of fixing a simple config bug. Instead of asking AI to directly write the fix, he asked it to investigate dependencies, identify follow-up actions, and create a plan with multiple alternatives. He, the human, then reviewed output and made the final call. 

Generally, this framework makes sense and mirrors how I use Claude on a daily basis when working through tickets. But there are also a few practical gotchas with this approach worth discussing. 

### Do you have the ability to effectively QA an AI's output?
Your ability to verify AI output is dictated by your current level of mastery over that specific domain. The conventional wisdom of "don't delegate what you cannot do yourself" applies here. If you delegate something you haven't had the chance to grasp fully, you risk never developing the intuition required to verify the AI's work. 

My approach to solving this routinely picking tasks that are important, but not in the critical path, to build manual "reps". Honestly though, this is incredibly hard to do on the job. As an engineering manager, I am routinely forced to take up time-sensitive tasks and context switch constantly. My afternoons are often blocked with meetings and 1:1s with very little focus time. I often find myself spending time after hours building foundational projects from scratch - like doing a codecrafters.io challenge to build a Claude Code clone or a Redis clone - just to intentionally step back into the trenches so that I can maintain my edge. 

### Can you clearly separate "mechanical" work from "decision-making" work?
This clean separation is necessary to delegate the former to AI while reserving the latter for human judgement. But is this line always clear? If an AI investigates a bug and presents you three alternatives, isn't it already steering your executive judgement? A human executive reviewing three alternatives presented by AI might pick the "best" of the three without asking if there is a fundamental redesign that eliminates the bug entirely (see [Framing Effect](https://thedecisionlab.com/biases/framing-effect)). 

My strategy here is to engage with the AI's output through Socratic questioning. I deliberately go down rabbit holes challenging assumptions, similar to how a good executive might interrogate a subordinate's report. I even created a Claude skill for this purpose. But doing this constantly is exhausting, and scales poorly under time pressure. 

---

**Ultimately, the engineer-as-executive model is powerful**, but it assumes we always have the time and discipline to manage our AI subordinates effectively. Right now, balancing that discipline against the velocity of the job remains an unsolved problem for me. The solution is likely going to take the shape of automated guardrails that allows humans to confidently take a step back from reviewing everything an AI does but we're not fully there yet. 
