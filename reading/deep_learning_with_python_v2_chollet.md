# Deep Learning with Python

## Second Edition

### Francois Chollet

---

## Preface

- Progress of deep learning in AI
- Near unusable computer vision & NLP to high performance deployed at scale.
- Applications in every industry.
  - Medical Imaging
  - Agriculture
  - Autonomous Driving
  - Education
  - Disaster Prevention
  - Manufacturing
- Even with this progress, field still in early days
- Small fraction of potential realized
- Need to make DL as accessible as possible
- Radical democratization
- Move it out of the ivory tower into the hands of everyone
- Almost anyone can now build a website or web app for their business or community of a kind that would have required a small team of specialist engineers in 1998. In the not-so-distant future, anyone with an idea and basic coding skills will be able to build smart applications that learn from data.


**Keras and TensorFlow best practives as of 2021**

- After reading this book, you’ll have a solid understand of what deep learning is, when it’s applicable, and what its limitations are. 
- You’ll be familiar with the standard workflow for approaching and solving machine learning problems, and you’ll know how to address commonly encountered issues. 
- You’ll be able to use Keras to tackle real-world problems
  - Computer vision
  - Natural language processing
  - image classification
  - image segmentation
  - timeseries forecasting
  - text classification
  - machine translation
  - text generation, and more.

[Book Forum](https://livebook.manning.com/#!/book/deep-learningwith-python-second-edition/discussion)

[Manning websit](https://www.manning.com/books/deep-learning-with-python-second-edition)

[Jupyter notebooks on GitHub](https://github.com/fchollet/deep-learning-with-pythonnotebooks)

---

# Chapter 1


## What is deep learning?

>High0level definitions of fundamental concepts
>Timeline of ML development
>Key foactors of popularity and future potential

### AI, ML, DL...

**AI:** 
- Born in 1950s
- Can computers "think"?
- 1956 | John McCarthy | Dartmouth
- DEFINITION
  - *the effort to automate intellectual tasks normally performed by humans*]
- Early efforts attempted to hard code a lot of thing with a series of explicit rules. Known as *symbolic AI* dominant from 1950s-1980s. 
- Suitable to solve well-defined, logical problems like playing chess - useless for image, speech, nlp, etc.

**Machine Learning:**
- Lady Ada Lovelave | Charles Babbage *Analytical Engine* First known general-pourpose mechanical computer. 

>*The Analytical Engine has no pretensions whatever to originate anything. It can do whatever we know how to order it to perform. . . . Its province is to assist us in making available what we’re already acquainted with.*

 - Even with 178 years of historical perspective, Lady Lovelace’s observation remains arresting. 
   - Could a general-purpose computer “originate” anything, or would it always be bound to dully execute processes we humans fully understand? 
   - Could it ever be capable of any original thought? 
   - Could it learn from experience? 
   - Could it show creativity?

Her remark was later quoted by AI pioneer Alan Turing as “Lady Lovelace’s objection” in his landmark 1950 paper “Computing Machinery and Intelligence,”1 which introduced the *Turing test* as well as key concepts that would come to shape AI.

Tueing was of the opinion—highly provocative at the time—that computers could in principle
be made to emulate all aspects of human intelligence.

The usual way to make a computer do useful work is to have a human programmer write down rules—a computer program—to be followed to turn input data into appropriate answers, just like Lady Lovelace writing down step-by-step instructions for the Analytical Engine to perform. 

Machine learning turns this around: the machine looks at the input data and the corresponding answers, and figures out what the rules should be.

A machine learning system is *trained* rather than explicitly programmed.

- It’s presented with many examples relevant to a task, and it finds statistical structure in these examples that eventually allows the system to come up with rules for automating the task.
- For instance, if you wished to automate the task of tagging your vacation pictures, you could present a machine learning system with many examples of pictures already tagged by humans, and the system would learn statistical rules for associating specific pictures to specific tags.
- Although machine learning only started to flourish in the 1990s, it has quickly become the most popular and most successful subfield of AI, a trend driven by the availability of faster hardware and larger datasets.
- Unlike statistics, machine learning tends to deal with large, complex datasets (such as a dataset
of millions of images, each consisting of tens of thousands of pixels) for which classical statistical analysis such as Bayesian analysis would be impractical.
- As a result, machine learning, and especially deep learning, exhibits comparatively little mathematical
theory—maybe too little—and is fundamentally an engineering discipline.

- To do machine learning, we need three things:
  - *Input data points*—For instance, if the task is speech recognition, these data
points could be sound files of people speaking. If the task is image tagging, they
could be pictures.
  - *Examples of the expected output*—In a speech-recognition task, these could be
human-generated transcripts of sound files. In an image task, expected outputs
could be tags such as “dog,” “cat,” and so on.
  - *A way to measure whether the algorithm is doing a good job* —This is necessary in order to determine the distance between the algorithm’s current output and its expected output. The measurement is used as a feedback signal to adjust the way the algorithm works. This adjustment step is what we call learning.

- *Learning*, in the context of machine learning, describes an automatic search process for data transformations that produce useful representations of some data, guided by some feedback signal—representations that are amenable to simpler rules solving the task at hand.

- Machine learning algorithms aren’t usually creative in finding these transformations;
they’re merely searching through a predefined set of operations, called a *hypothesis space*.

- So that’s what machine learning is, concisely: searching for useful representations and rules over some input data, within a predefined space of possibilities, using guidance from a feedback signal. 
- This simple idea allows for solving a remarkably broad range of intellectual tasks, from speech recognition to autonomous driving.

### The “deep” in “deep learning”

- Deep learning is a specific subfield of machine learning: a new take on learning representations
from data that puts an emphasis on learning successive layers of increasingly meaningful representations. 
- Tje “deep” in “deep learning” isn’t a reference to any kind of deeper understanding achieved by the approach; rather, it stands for this idea of successive layers of representations. 
- How many layers contribute to a model of the data is called the depth of the model.



