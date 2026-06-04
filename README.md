# Trigram Laguage Model from Statistical Frequency

We humans use language flawlessly. But how can a computer generate language? These algorithmic machines do not understand. They can do things they are programmed on. Language generation comes from understanding, but this can be programmed too, thanks to decades of research! I'll explain the mechanism of a language generation model I've made.

> **Quick note:** I've learned Bigram language model from Andrej Karapathy's Makemore tutorial. After finishing the tutorial, I've coded this Trigram model to prove I'm not overfitted on Andrej Karapathy's awesome explaination!

---

## The complete breakdown

### Loading dataset
We load our dataset at first. In this project, I'm using Karapathy's dataset which contains ~32,000 names of people. We load this dataset in *words* variable as a list; each name is an item of the list. You can find the dataset [here](https://raw.githubusercontent.com/karpathy/makemore/master/names.txt).

---

## How a trigram model works (The high level logic)
A trigram model works by predicting the next character **with context of previous 2 characters**. It's better than a bigram model because it uses more context to predict the next character.

Let's say, a trigram model predicts 
