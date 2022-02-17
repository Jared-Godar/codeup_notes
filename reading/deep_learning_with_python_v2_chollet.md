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





