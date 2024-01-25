# MLSys-NYU-2023
Slides, scripts and materials for the Machine Learning in Finance course at NYU Tandon, 2023.

## Overview

DISCLAIMER: A significant part of our course is class participation (this is why, in the end, we have universities and not *just* repos!), and no amount of scripts can provide the same level of educational content, or a comparable experience. Please note that this course changes substantially every year, so the best way to keep up to date with us is... by enrolling in the [Master](https://engineering.nyu.edu/academics/programs/financial-engineering-ms)!

TL;DR: This repository contains some of the teaching materials by Prof. [Ethan Rosenthal](https://www.ethanrosenthal.com/) and [myself](https://jacopotagliabue.it/) for the 2023 course in ML at the NYU Tandon School of Engineering. The course is presented as an introduction to Machine Learning with finance-motivated use cases and industry-standard tools.

We open source slides and assignments months after the class is completed, hoping to benefit the broader community of students and practitioners; I had a calculus book that said, "What one fool can do, another can.", and we all wish more and more fools could become proficient at building reliable, trust-worthy, well-crafted ML systems.

We feel there are now enough books and YouTube videos for people interested in the theory of ML; moreover, practitioners produce a much bigger marginal value when bringing into the class their day-to-day experience, which, for the time being, cannot be as easily found on YouTube. Therefore, the course we run is very practical and focuses on the intuitive understanding of ML problems and their solutions _through real-world tools_: we emphasize the importance of good coding habits, and the use of industry standard methodology, over complex modelling and formulas (alas, we do indeed sometimes need to talk about math).

The whole course runs in 14 weeks, but we cover arguments that would keep you busy for a lifetime: every lecture is the result of explicit and implicit trade-offs - what should we cover, what should we not? While no material can substitute for real-world interactions and our great sense of humour, we leave for the open source community to judge how useful the trade-offs we picked actually are.

## At a glance

### Main themes

The course is structured around 14 weeks: 13 weeks of lectures, and 1 final demo day for students to present an end-to-end machine learning project that showcases what they learned in the course. Roughly speaking, the first half of the course is focused on "how do I make sure I have a decent repository ?"

### Repo structure

The epository is partitioned by week: each week has its folder, with a self-contained `README`, scripts / notebooks and slides. Note that this year we used [rye](https://rye-up.com/guide/) for Python dependency management. The choice results in some redundancy, but provides more clarity for students pacing themselves through the course, and highlights the highly modular nature of the syllabus.

### Changelog

Compared to [2022 edition](https://github.com/jacopotagliabue/MLSys-NYU-2022), a lot has changed. As a non-exhaustive list:

* new introducton to Python dependency management with Rye;
* introduction to deep learning;
* use case based lectures by finance professionals;
* RecSys section has been replaced by an introduction to NLP, with a focus on the basics of language modelling.

## Acknowledgments

Thanks to all outstanding people quoted and linked in the slides: this course is possible only because we truly stand on the shoulders of giants. Special thanks also to:

* [Hugo](https://www.linkedin.com/in/hugo-bowne-anderson-045939a5/) and [Eddie](https://www.linkedin.com/in/eddie-mattia/) for being the best Metaflow teachers on the planet;
* [Joao](https://joao.ai/) for being our fantastic guest speaker on data science in finance.

## Suggested complementary / additional readings

The main topics are all huge, and we could obviously just scratch the surface. Aside from all the references to be found in the slides and READMEs, these are few good places to further explore this world.

### Machine Learning
* [Deep Learning with Python](https://www.amazon.com/Learning-Python-Second-Fran%C3%A7ois-Chollet/dp/1617296864): great practical intro to ML concepts and the basics of DL using Keras.

* [Machine Learning with PyTorch and Scikit-Learn](https://www.amazon.com/Machine-Learning-PyTorch-Scikit-Learn-learning-ebook/dp/B09NW48MR1): another great practical intro to ML / DL, focused on PyTorch.

### MLOps
* [Designing Machine Learning Systems: An Iterative Process for Production-Ready Applications](https://www.amazon.com/Designing-Machine-Learning-Systems-Production-Ready/dp/1098107969): a book by Chip Huyen on how machine learning systems are designed.

* [Effective Data Science Infrastructure](https://www.manning.com/books/effective-data-science-infrastructure): a book by Ville Tuulos on how to make data scientist productive.

* [You Don't Need a Bigger Boat](https://github.com/jacopotagliabue/you-dont-need-a-bigger-boat): our own fully open source repository showing how state-of-the-art ML systems can be built at scale, component after component.

* [Comet for Data Science](https://www.packtpub.com/product/comet-for-data-science/9781801814430): on how to take advantage of existing platform for experiment tracking, collaboration and managing the life-cycle of ML artifacts.

## Contacts

For questions, feedback, comments, please drop me a message at: `jacopo dot tagliabue at nyu.edu`.
