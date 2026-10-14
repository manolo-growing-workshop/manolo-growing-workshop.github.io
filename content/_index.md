---
title: Home
---

## About

Deep learning has scaled remarkably well, but the model sizes needed for state-of-the-art results are growing exponentially and outpacing hardware improvements. Can we use parameters more efficiently?

Almost all of the literature assumes a *fixed* architecture: choose a model, then train it. A rapidly growing body of work breaks that assumption and changes the trainable structure *during* optimization. Examples include:

- growing neurons and layers
- stacking and progressive scaling of transformers
- dynamic sparse training and prune-and-regrow schemes that rewire the network's topology as it learns
- modular expansion for non-stationary tasks in continual and reinforcement learning

In each case, capacity is decided during training rather than fixed in advance, so parameters are used only where and when they are useful.

## The open problem

These methods share one unresolved problem: **once the trainable structure changes, how should optimization continue?** A growth step changes the set of trainable parameters, and with it the optimizer state, learning-rate schedule and normalization statistics. Handling these badly can destroy trainability even when the new architecture is well motivated. Open questions include:

- *When* and *where* should a model change its structure within a single training run?
- How should parameters, optimizer state and normalization statistics be transferred across a growth step?
- How can training be stabilized immediately afterwards?
- How can we measure the quality of a growth transition?

## Why this workshop

This line of work is split across the growth, sparse-training, continual-learning, reinforcement-learning and optimization communities. Each uses its own vocabulary, baselines and evaluation practices, and there is little direct collaboration between them. This one-day workshop brings these groups into one room to build a shared understanding of the problem before the field fragments further into method-specific benchmarks.

It is also a deliberately frugal research direction, in line with the goals of the MANOLO project: progress comes from algorithmic insight rather than compute budget, which makes the area accessible to smaller labs priced out of large-scale deep learning.

The day features six invited talks, a poster session over lunch, and a closing panel discussion. See the [programme]({{< relref "programme" >}}) and the [call for posters]({{< relref "call-for-posters" >}}).

## Important dates

{{< dates >}}

## Invited speakers

{{< people "speakers" >}}

## Organizers

{{< people "organizers" >}}
