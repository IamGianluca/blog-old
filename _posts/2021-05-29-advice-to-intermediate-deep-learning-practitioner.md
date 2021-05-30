---
toc: true
layout: post
description: How to increase your productivity and become more effective
categories: [deep learning, machine learning, productivity]
title: Advise to an intermediate Deep Learning practitioner
---

# Intro

This article is aimed to practitioners with at least a couple of years of experience. You should be familiar with the fundations of Machine Learning and have at least three (or more) projects. My goal is to share my experience on how you can increase your productivity as a Machine Learning and Deep Learning practitioner.

Generally speaking, three things can help you become more productive:
* Know what you're doing
* Iterate faster
* Have an effective development environment

We will see how these themes will come up repeatedly in this article. 

# Learn how to code 

The best investment in your productivity is to learn how to code. This means writing code that is reusable and modular. [Don't Repeat Yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) and [Keep It Simple (Stupid)](https://en.wikipedia.org/wiki/KISS_principle).

Refactor your code often. Don't procrastinate when you notice things that can be improved in the codebase. [Cruft](https://martinfowler.com/bliki/TechnicalDebt.html) accumulates rapidly and in no time it will prevent you from iterate quickly. Refactoring is a critical component of the development lifecycle. Don't neglect that.

There are two books I often recommend about good software development practices:
* ["Clean Code" by Robert Cecil Martin](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
* ["Refactoring" by Martin Fowler](https://martinfowler.com/books/refactoring.html)

Two key points here are consistency and discipline. You will get there!

# Master your tools

As a Machine Learning practitioner, you will spend lots of your time working on a codebase, often in a remote Linux server. There are some tools you must learn how to use well if you want to be effective. These include:
* Git
* Linux
* Docker

Some tools I often recommend are:
* [tmux](https://github.com/tmux/tmux)
* [powerline-shell](https://github.com/b-ryan/powerline-shell)
* [dvc](https://github.com/iterative/dvc): Think about it as Git for Machine Learning

I would also recommend you to use dotfiles manager. There are many options out there. Choose one that works for you. Ideally, you would like to install your dotfiles in a new machine with one command. 

I would also recommend you to choose some popular ML libraries and stick to them unless there is a clear advantage in switching to a new one. The software engineering and ML worlds are moving rapidly, and new tools are released seamingly weekly. Your goal is to be effective at build things, not learning how to master the lastest fancy tool.

### Become one with your IDE

Mastering your IDE is essential. You will spend lots of time in it. You better be familiar with how to get the best out of it. Learn keybindings and keyboard shortcuts for those operations you do regularly. Learn how to rapidly navigate the codebase ― e.g., jump to definition, rename a symbol, etc. Research which plugins could help you become more productive, but don't go too crazy with plugins. The faster you navigate a project, the quicker you can familiarize with it, implement new features, and fix bugs. 

Additionally, every time you notice a repeated pattern, search how you could automate it. A few minutes per day saved will accumulate and leave you more time to think/work on more valuable tasks.

Avoid religious wars about IDEs. Choose what's best for you and stick to it. I would also recommend you to stay away from people that are too opinionated about IDEs.

### Be comfortable with using a debugger

Bugs happen. Being able to interpret error messages and finding the root cause is critical to move fast. Read the error message. Follow the traceback to identify which line is triggering the error. Jump to that line in the codebase and analyze what is wrong. It is really that simple.

# Iterate fast

When starting a new project, you need to have a clear plan for making rapid sustainable progress.

### Define ML pipeline first

Start by building a skeleton for the ML pipeline. Implement all the necessary steps ― e.g., download, unzip, create folds, preprocess, train, predict, post-process ― without worrying too much about the overall solution. Simplify things as much as possible. Just make sure you have a pipeline you can rapidly improve on.

### Cross-validation

Once the initial ML pipeline is ready, it's time to focus on building a robust validation strategy. [Rachel Thomas](https://twitter.com/math_rachel) wrote a [brilliant blog article](https://www.fast.ai/2017/11/13/validation-sets/) about it. I would recommend you to read it, if you haven't already. 

Remember, cross-validation is the crucial for making rapid progress. If you don't have confidence in your validation strategy, you can't trust the results of your experiments.

### Choose a good evaluation metric

This is another thing I've seen many get wrong. Think about what is your ultimate goal, and play with the metric. Is the metric rewarding/penalizing models appropriately to your goal? It would be a waste of time to spend months improving on a metric to discover that it doesn't align with the business goals.

### Sample data

Most of the time, there is no need to use all the available data to test some ideas. Make sure you're working with enough data to have confidence in the results but little enough to be able to iterate quickly. The faster you iterate, the more ideas you can test, and the more progress you will make. [Learning curves](https://scikit-learn.org/stable/modules/learning_curve.html#learning-curve) help identify a reasonable threshold for how much data you need.

Of course, use all data available when training your final model(s). But for rapid development purposes, if you can get the same answers in half the time, that's huge.

### Start with a simple baseline

Start easy. Don't jump immediately to the latest fancy model/architecture. Begin with a linear model or even simple frequencies. Once you have established a baseline, try to improve on that. Do it gradually, though.

I've seen plenty of colleagues wasting months of work developing a fancy deep learning solution to discover that a simple linear model worked better.

### Use your brain

Too often, I see young practitioners trying things without having a real plan. Make sure you know how to diagnose if your model is underfitting or overfitting, and know how to address that. Formulate hypotheses and run experiments to validate them. If the experiment is not successful, make sure you understand why. That is how you build lasting knowledge. Don't try random things in the hope of getting lucky. That is not effective.

There are massive non-linearities in input and output between top practitioners and the rest of the field. Top practitioners know what to do and why. Being "right" for the wrong reasons does not guarantee long-term success in this profession. You want to be "right" for the correct reasons. Be honest with yourself. That will pay off in the long term. 

One great resource for learning how to be an effective ML practitioner is ["Machine Learning Yearning" by Andrew Ng](https://www.deeplearning.ai/programs/). The book is still under development, but you can get free access to the most recent draft.