# Week 14

## Demo day

How to know you are ready? The checklist in [Week 11](https://github.com/jacopotagliabue/MLSys-NYU-2023/blob/main/weeks/11/Project_checklist.pdf) is a good start, together with the discussions we had in class.

### Presentation rules / guidelines

We have 11 teams, and each will have a max of 9 minutes for presentation and 2 for Q&A.

* Choose the speaker(s) and _make sure (by rehearsing many times!) that your presentation is done in 9 minutes_: we will cut your presentation (and grade) if you don't respect the timing.
* Explain clearly the problem, assuming we are not familiar with it: why did you pick it? Why is it important for a business? Why is it hard? If helpful, pretend to be actually an employee of the target company building the actual system (e.g. fraud detection for American Express): what should you pay attention to?
* Explain clearly the choices you made, but only go deep in the insightful / interesting stuff: do _not_ list the features you use, or the steps in your pipeline, but try to tell a story: what did you learn? Did you succeed or was the problem too hard (it is fine if it was, the point here is about building the pipeline)? Was there something you first tried and then changed? What would you do with more time? Code details are part of the deliverables (see below), but they are not that important for your presentation: assume you are talking to colleagues, and try to communicate just what is essential for them to make them understand / aware of the challenges and your solution.
* Another way to see this: imagine to present your slides / demo to yourself as you were _when this course started_ - would you like it? Would you be able to follow the main arguments?
* Your final deliverables to your TA are: the slides / demo you present in class, _and_ the entire ML project as a stand-alone GitHub repository: make sure your repository contains all the necessary ingredients to be understood, reproduced, and evaluated (a well-written README, requirements / poetry files, screenshots on what to expect on Comet etc.).

Good luck!

### Evaluation criteria for the final project

As per your Syllabus, the Final Project is 30% of the course grade. Your project will be scored by averaging grades on three main dimensions, which reflect the content of the course:

* project structure / coding (evaluated by the TA): the grade reflects how well the project is organized and how clear is the coding wrt the aspects we stressed in class: for example, is the README clear? Can the flow be easily reproduced? Are requirements specified? Do functions have types and comments?
* ML (TA): the grade reflects the quality of the data science work to solve the problem: for example, is EDA insightful? Are good qualitative tests implemented? Is the model appropriate for the task? How is evaluation performed? Which metrics have been used and why? Are you tracking experiments on Comet etc.?
* Project presentation (Prof. Ethan and Prof. Jacopo for presentation, TA for deployment): the grade reflects the ability to "think end-to-end", that is, going from a challenge you find interesting, to a full ML pipeline that attempts to solve that challenge. Is the problem well explained? Is the choice of data, models, metrics appropriate for the challenge? Is "success" clearly defined? Is the demo compelling? Can the model be used in an app / endpoint etc.?

Please make sure you deliver the project to your TA as a GitHub repository he can access, containing all the code / notebooks you used for the project, all the slides / comet screenshots etc. and (see above) a clear, complete README that explains how to set up the environment, run the code, and what to expect. Do NOT commit to GitHub credentials for AWS, Comet etc..
