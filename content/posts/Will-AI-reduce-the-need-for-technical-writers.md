---
title: Will AI reduce the need for technical writers?
date: '2019-01-11T15:01:00.833Z'
excerpt: >-
  The late Stephen Hawking famously said that artificial intelligence would be
  “either the best, or the worst thing, ever to happen to…
thumb_img_path: >-
  images/Will-AI-reduce-the-need-for-technical-writers/1*rsEC26fuirCnU8f31OHbBQ.jpeg
layout: post
---
The late Stephen Hawking famously said that artificial intelligence would be “either the best, or the worst thing, ever to happen to humanity.” As a technical writer documenting AI technology, I’d like to believe it would be the former and it’s fair to say there have already seen positive signs about how AI might shape and assist with documentation in the future.

![](/images/Will-AI-reduce-the-need-for-technical-writers/1*rsEC26fuirCnU8f31OHbBQ.jpeg)

A number of tech companies have already dipped their toes into the water, with some developing AI-assisted, predictive content generation and others harnessing machine learning to predict the help content the end-user is looking for.

### Trending AI Articles:

> [1\. How to train a neural network to code by itself ?](https://becominghuman.ai/how-to-train-a-neural-network-to-code-by-itself-a432e8a120df)

> [2\. Paper repro: “Learning to Learn by Gradient Descent by Gradient Descent”](https://becominghuman.ai/paper-repro-learning-to-learn-by-gradient-descent-by-gradient-descent-6e504cc1c0de)

> [3\. Reinforcement Learning for Autonomous Vehicle Route Optimisation](https://becominghuman.ai/reinforcement-learning-for-autonomous-vehicle-route-optimisation-d97efec9abbd)

> [4\. Best websites a programmer should visit in 2018 @code\_wonders](https://becominghuman.ai/code-wonders-96d629bb8d8c)

### AI-assisted content writing

Google introduced its natural language processing development, Smart Compose, to help Gmail users write emails in May 2018. They combined a [bag-of-words](https://en.wikipedia.org/wiki/Bag-of-words_model) (BoW) model with a [recurring-neural-network](https://en.wikipedia.org/wiki/Recurrent_neural_network) (RNN) model to predict the next word or word sequence the user will type depending on the prefix word sequence previously typed.

![](/images/Will-AI-reduce-the-need-for-technical-writers/1*1M0p004ntq6pNz6cPYC6PQ.png)

<figcaption>The Google Smart Compose RNN-LM model architecture.</figcaption>

Smart Compose was trained with a corpus of billions of words, phrases and sentences, and Google carried out vigorous testing to make sure the model only memorised the common phrases used by its many users. The Google team admits it has more work to do and is working on incorporating their own personal language models that will more accurately emulate each individual’s style of writing.

Arguably one of their biggest challenges they face is reducing the human-like biases and subsequent unwanted and prejudicial word associations that AI inherits from a corpus of written text. Google cited [research](http://www.cs.bath.ac.uk/~jjb/ftp/CaliskanEtAl-authors-full.pdf) by Caliskan et al which found that machine learning models absorbed stereotyped biases. At the most basic level, the models associated floral words with something pleasant and insect words with something unpleasant. More worryingly, they also found the machine-learning models adopted racial and gender biases.

![](/images/Will-AI-reduce-the-need-for-technical-writers/1*6asmr42GvxhMUojtx0eKaA.png)

<figcaption>Caliskan et al found AI models absorbed gender and racial biases from a large body of&nbsp;text.</figcaption>

The researchers found that a group of European American names were more readily associated with pleasant than unpleasant terms when compared to a batch of African American names. They also found inherited biases included associating female names and words with family and the arts while male names were associated with career and science words.

Yonghui Wu, the principal engineer from the Google Brain team, said: “…these associations are deeply entangled in natural language data, which presents a considerable challenge to building any language model. We are actively researching ways to continue to reduce potential biases in our training procedures.”

### AI-assisted spelling and grammar

With 6.9 million daily users, one of the most common tools people are using to assist with the accuracy of their spelling and grammar is Grammarly. The company are experimenting with AI techniques including machine learning and natural language processing so the software can essentially understand human language and come up with writing enhancements.

![](/images/Will-AI-reduce-the-need-for-technical-writers/1*35DDZmvwmqdn6FdBYvhkxg.jpeg)

Grammarly has been training different algorithms to measure the coherence of naturally-written text using a corpus of text compiled from public sources including Yahoo Answers, Yelp Reviews and government emails. The [models they have experimented](https://www.grammarly.com/blog/detecting-disorganized-writing-with-ai/) with include:

*   **Entity-based model** — Tracks specific entities in the text. For example, if it finds the word “computer” in multiple sentences it assumes they are related to each other.
*   **Lexical coherence graph** — Treats sentences as nodes in a graph with connections (“edges”) for sentences that contain pairs of similar words. For example, it connects sentences containing “macbook” and “chromebook” because they are both probably about laptop computers.
*   **Deep learning model** — Neural networks that capture the meaning of each sentence and are able to combine these sentence representations to learn the overall meaning of a document.

Although this is still a work in progress, Grammarly’s long term goal long term isn’t just to point out spelling and grammatical mistakes. They hope their machine-learning models will be able to inform you how coherent your writing is and also highlight which passages are difficult to follow.

### AI-assisted help content

Some companies have also started to look at ways that AI can help with predicting and directing readers to the exact content they are looking for. London-based smart bank Monzo launched a [machine-learning powered help system](https://monzo.com/blog/2017/05/03/practical-machine-learning-for-startups/) for their mobile app in August 2017.

![](/images/Will-AI-reduce-the-need-for-technical-writers/1*BFuprn4ar_R20w2i5kB3aQ.jpeg)

Their data science team trained a model of recurring-neural-networks (RNNs) with commonly asked customer support questions to make predictions based on a sequence of actions or “event time series”. For example:

User logs in → goes to **Payments** → goes to **Scheduled payments →** goes to **Help**.

At this point, the help system provides suggestions relating to payments and as the user starts typing, returns common questions and answers relating to scheduled payments. Their initial tests showed they were able to reach 53% accuracy when determining the top three potential categories that users were looking for out of 50 possible support categories. You can read more about their help search algorithm [here.](https://monzo.com/blog/2017/08/22/the-help-search-algorithm/)

### What does the future hold?

I think we will see more content composition tools like Smart Compose emerge but it will take a lot of time and work before they can be trained to effectively assist with the complex and often unpredictable user-oriented content that technical writers are tasked with producing on a daily basis.

![](/images/Will-AI-reduce-the-need-for-technical-writers/0*9NMvTtjb8x31evnl.jpg)

I’m sure some technical writers are already using Grammarly to assist with their spelling and grammar. It can be a really powerful tool to ensure your text is not only accurate but in the future it will be able to measure whether your writing is actually coherent and readable. I’ve dabbled with Grammarly but found it either wasn’t compatible with certain tools or prevented some of my applications from working so it became a bit of hindrance rather than an assistant for me personally. No doubt these are kinks they will iron out at some point down the line.

I do see the benefits of AI-assisted help like Monzo have created so it would be awesome to see some more development in this area. It could potentially be something that saves customer support and documentation teams a lot of time in terms of predicting and directing end-users to answers before they’ve even asked a question.

So are we there yet? Not quite… but I think some very promising foundations have been laid. While some technical writers might be concerned, I think it will be a very long time before AI is advanced enough to supplant our role in the development teams. So don’t be afraid of AI, for the time being these tools are only going to make our lives easier!

### **References:**

1.  Stephen Hawking: Will AI kill or save mankind? [https://www.bbc.co.uk/news/technology-37713629](https://www.bbc.co.uk/news/technology-37713629)
2.  Smart Compose: Using Neural Networks to help write emails: [https://ai.googleblog.com/2018/05/smart-compose-using-neural-networks-to.html](https://ai.googleblog.com/2018/05/smart-compose-using-neural-networks-to.html)
3.  Semantics derived automatically from language corpora contain human-like biases: [http://www.cs.bath.ac.uk/~jjb/ftp/CaliskanEtAl-authors-full.pdf](http://www.cs.bath.ac.uk/~jjb/ftp/CaliskanEtAl-authors-full.pdf)
4.  Grammarly Spotlight: How we use AI to enhance your writing: [https://www.grammarly.com/blog/how-grammarly-uses-ai/](https://www.grammarly.com/blog/how-grammarly-uses-ai/)
5.  Under the Hood at Grammarly: Detecting Disorganized Writing with AI: [https://www.grammarly.com/blog/detecting-disorganized-writing-with-ai/](https://www.grammarly.com/blog/detecting-disorganized-writing-with-ai/)
6.  Practical Machine Learning with Event Streaming: [https://monzo.com/blog/2017/05/03/practical-machine-learning-for-startups/](https://monzo.com/blog/2017/05/03/practical-machine-learning-for-startups/)
7.  The Help Search Algorithm: [https://monzo.com/blog/2017/08/22/the-help-search-algorithm/](https://monzo.com/blog/2017/08/22/the-help-search-algorithm/)

### Don’t forget to give us your 👏 !

![](/images/Will-AI-reduce-the-need-for-technical-writers/0*Co8-_Yc-CtGgCRr7.jpg)

<iframe src="https://upscri.be/8f5f8b?as_embed=true" width="700" height="350" frameborder="0" scrolling="no"></iframe>

[![](/images/Will-AI-reduce-the-need-for-technical-writers/1*2f7OqE2AJK1KSrhkmD9ZMw.png)](https://becominghuman.ai/artificial-intelligence-communities-c305f28e674c)

[![](/images/Will-AI-reduce-the-need-for-technical-writers/1*v-PpfkSWHbvlWWamSVHHWg.png)](https://upscri.be/8f5f8b)

[![](/images/Will-AI-reduce-the-need-for-technical-writers/1*Wt2auqISiEAOZxJ-I7brDQ.png)](https://becominghuman.ai/write-for-us-48270209de63)
