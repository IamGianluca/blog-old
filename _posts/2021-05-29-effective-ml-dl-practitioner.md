---
toc: true
layout: post
description: Increase you productivity and build lasting knowledge
categories: [deep learning, machine learning, productivity]
title: How to become a more effective ML/DL practitioner
---

# Intro

This article is aimed to any practitioners that wants to become more effective. This is of course just my opinion, but I hope it will help many people struggling to make the next step in their career. I've shared many of this tips over the years and seen the powerful effect they had both on me and others.

Before we start, I'm expecting you to know very well the fundations of Machine Learning. This is necessary prerequisite for anyone working as a Data Scientist or Machine Learning engineer. After you have acquired a good understanding of the fundamentals, there are generally three things that will help you become more productive:
* Have an effective development environment
* Iterate faster
* Continuous learning 

We will see how these themes will come up repeatedly in this article. 

# Learn how to code 

The best investment in your productivity is to learn how to code properly. This means writing code that is reusable and modular. [Don't Repeat Yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) and [Keep It Simple (Stupid)](https://en.wikipedia.org/wiki/KISS_principle) should be your guiding principles.

Refactor your code often. Don't procrastinate when you notice things that can be improved in the codebase. [Cruft](https://martinfowler.com/bliki/TechnicalDebt.html) accumulates rapidly and in no time it will prevent you from iterate quickly. Refactoring is a critical component of the development lifecycle. Don't neglect that.

Try to be a good boyscout: 

> Always leave the campground cleaner than you found it.

Your goal is to help your future self. You want to write code once, and reuse it in the future when the need arise. You don't want to keep reimplementing the same function/class over and over again. You want to go out and accomplish bigger things.

There are two books I often recommend about good software development practices:
* ["Clean Code"](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882) by [Robert C. Martin](https://twitter.com/unclebobmartin)
* ["Refactoring"](https://martinfowler.com/books/refactoring.html) by [Martin Fowler](https://twitter.com/martinfowler)

Two key points here are consistency and discipline. You will get there!

# Master your tools

As a Machine Learning practitioner, you will spend lots of your time working on a codebase, often connecting to a remote Linux server. There are some tools you must learn how to use well if you want to be effective. These include:
* Git
* The Linux command line
* Docker

Other tools I often recommend are:
* [tmux](https://github.com/tmux/tmux)
* [powerline-shell](https://github.com/b-ryan/powerline-shell)
* [dvc](https://github.com/iterative/dvc)

I would also recommend you to use a dotfiles manager. There are many options out there. Choose one that works for you. Ideally, you would like to install your dotfiles in a new machine with just one command. 

I would also recommend you to choose some popular ML libraries and stick to them unless there is a clear advantage in switching to a new one. The software engineering and ML worlds are moving rapidly, and new tools are released seamingly weekly. Your goal is to be effective at build things, not learning how to master the lastest fancy tool.

### Become one with your IDE

Mastering your IDE is essential. You will spend lots of time in it. You better be familiar with how to get the best out of it. Learn keybindings and keyboard shortcuts for those operations you do regularly. Learn how to rapidly navigate the codebase ― e.g., jump to definition, rename a symbol, etc. The faster you navigate a project, the quicker you can familiarize with it, implement new features, and fix bugs. 

![]({{ site.baseurl }}/images/toolbox.jpg "Fig 1: As a good craftsman, you must become one with your tools.")

Additionally, every time you notice a repeated pattern, search how you could automate it. A few minutes per day saved will accumulate and leave you more time to think/work on more valuable problems.

Avoid religious wars about IDEs. Choose what's best for you and stick to it. I would also recommend you to stay away from people that are too opinionated about IDEs.

### Be comfortable with using a debugger

Bugs happen. Being able to interpret error messages and identify the root cause is critical to move fast. Read the error message. Follow the traceback to discover which line is triggering the error. Jump to that line in the codebase and analyze what is wrong. It is really that simple.

# Iterate faster

When starting a new project, you need to have a clear plan for making rapid sustainable progress.

### Visualize the data

Many practitioners spend too little time familiarizing with the data. They simply load it in a DataLoader and pass it to a model. That might give you the false feeling of moving fast, but moving fast is worthless if you're going in the wrong direction.

Spend at least a few hours plotting distributions, looking at images, and inspecting outliers. That will give you a good understanding of what problems your model might face, and ultimately guide your progress. 

You should not limit yourself to look at the data only at the beginning of a project. Use Error Analysis to understand what model improvement should lead the best return on investment.

### Define ML pipeline skeleton

Start by building a skeleton for the ML pipeline. Implement all the necessary steps ― e.g., download, unzip, create cross-validation folds, preprocess, train, predict, post-process ― without worrying too much about the overall solution. Keep things as simple as possible at this stage. Just make sure you have a pipeline you can rapidly improve on.

### Cross-validation

Once the initial ML pipeline is ready, it's time for you to focus on building a robust cross-validation strategy. [Rachel Thomas](https://twitter.com/math_rachel) wrote a [brilliant blog article](https://www.fast.ai/2017/11/13/validation-sets/) about it. I would recommend you to read it, if you haven't already. 

Remember, cross-validation is crucial for making rapid progress. If you don't have confidence in your validation strategy, you can't trust the results of your experiments. Even worse, if you cross-validation strategy is flawed, you will have the false impression of making progress.

### Choose a good evaluation metric

This is another thing I've seen many get wrong. Focus on the ultimate goal. Play around with the evaluation metric and ensure you understand how it behaves ― don't ignore the corner cases. Is the metric rewarding/penalizing models appropriately to your goal? It would be a waste of time to spend months improving on a metric to discover that it doesn't align with the business goals.

### Sample data

Most of the time, there is no need to use all the available data to test some ideas. Make sure you're working with enough data to have confidence in the results but little enough to be able to iterate quickly. The faster you iterate, the more ideas you can try, and the more progress you will make. [Learning curves](https://scikit-learn.org/stable/modules/learning_curve.html#learning-curve) help identify a reasonable threshold for how much data you need.

Of course, use all data available when training your final model(s). But for rapid development purposes, if you can get the same answers in half the time, that's huge.

### Start with a simple baseline

Start easy. Don't jump immediately to the latest fancy model/architecture. Begin with a linear model or even simple frequencies. Once you have established a baseline, try to improve on that. Do it gradually, though.

I've seen plenty of colleagues wasting months of work developing a fancy deep learning solution to discover that a simple linear model worked better because of a bug in their codebase.

### Be scientific

Too often, I see less experienced practitioners trying things without having a real plan. Make sure you know how to diagnose if your model is underfitting or overfitting, and know how to address that. Formulate hypotheses and run experiments to validate them. If the experiment is not successful, make sure you understand why. That is how you build confidence and lasting knowledge. Don't try random things in the hope of getting lucky. That is not effective.

![]({{ site.baseurl }}/images/scientific_method.png "Fig 2: The Scientific Method's workflow.")

There are massive non-linearities in input and output between top practitioners and the rest of the field. Top practitioners know what to do and why. Being "right" for the wrong reasons does not guarantee long-term success in this profession. You want to understand why something worked or did not. Be honest with yourself. That will pay off in the long term. 

One great resource for learning how to be an effective ML practitioner is ["Machine Learning Yearning"](https://www.deeplearning.ai/programs/) by [Andrew Ng](https://twitter.com/AndrewYNg). The book is still under development, but you can get free access to the most recent draft.