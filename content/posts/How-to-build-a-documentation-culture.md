---
title: How to build a documentation culture
date: '2019-08-30T19:00:05.033Z'
excerpt: >-
  Most programmers don’t like writing documentation, it’s just a fact. In some
  of the engineering teams I’ve worked in it’s often felt like…
thumb_img_path: images/How-to-build-a-documentation-culture/0*IudDafEKyWcFSb7W.jpg
layout: post
---
Most programmers don’t like writing documentation, it’s just a fact. In some of the engineering teams I’ve worked in it’s often felt like the annoying but necessary task that is left until the last minute or sometimes forgotten about altogether. However, documentation is important for a number of reasons:

*   If you have poor docs, users have to call or email your customer support team if they get stuck — this costs you money!
*   You risk increasing user frustration and dissatisfaction with your product if they can’t find out how to do something.
*   Good docs enable people to figure out how to do things for themselves, rather than having to interrupt experienced team members.
*   Without docs, you create knowledge silos where only a few engineers know how an aspect of your technology works. If these silos leave your team it creates knowledge gaps.

So, if you think documentation is lacking at your company, whether it is a tech startup or a mature software company, here are some things you can do to build a documentation culture.

### 1\. Find someone to drive it

If you don’t already have a technical writer, UX writer or content specialist in your team and you have the budget, then hire one! They will become the foundation of establishing your docs culture.

![](/images/How-to-build-a-documentation-culture/0*IudDafEKyWcFSb7W.jpg)

<figcaption>Photo by <a href="https://unsplash.com/@anniespratt?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" data-href="https://unsplash.com/@anniespratt?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Annie Spratt</a> on&nbsp;<a href="https://unsplash.com/search/photos/writer?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" data-href="https://unsplash.com/search/photos/writer?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Unsplash</a></figcaption>

Alternatively, you could try finding a “documentarian” — or “friend of the docs” — a programmer or perhaps a tester who is a good wordsmith and knows enough about your existing documentation and is willing to help drive the documentation effort.

### 2\. Create a style guide

You can establish some form of quality control by picking or writing a style guide. This becomes your reference to ensure consistency for things such as terminology and tone and voice.

If you don’t have the time or resources to write your own, you can adopt an existing one. Most technical writers refer to one of the following:

*   [Microsoft Style Guide](https://docs.microsoft.com/en-us/style-guide/welcome/) (formerly Microsoft Manual of Style)
*   [Chicago Manual of Style](https://www.chicagomanualofstyle.org/home.html)
*   [IBM style guide](https://www.ibm.com/developerworks/library/styleguidelines/)/ [The Red Hat Style Guide](http://stylepedia.net/style/)
*   [Google Developer Documentation Style Guide](https://developers.google.com/style/).

You will also find some useful style resources at [Write the Docs](https://www.writethedocs.org/guide/writing/style-guides/), a global community of people who care about documentation.

### 3\. Use spell checkers and linters

Another way to establish consistency in your technical content is to encourage the use of spell checkers and [linters](https://en.wikipedia.org/wiki/Lint_%28software%29). If you use open-source text editors like Atom or Sublime, you can install free spelling checking linters to help drive the accuracy and consistency of spelling and grammar.

![](/images/How-to-build-a-documentation-culture/1*r3naKFDa71a7ewQ4C_DJlA.gif)

Some linters and tools you could consider include:

*   [Alex](https://github.com/get-alex/alex): Linter available on multiple platforms.
*   [Hemingway](http://www.hemingwayapp.com/): App that checks content for passive voice and gives a readability score.
*   [Write Good](https://github.com/btford/write-good): Linter for English prose for developers.
*   [Vale](https://github.com/errata-ai/vale): A natural language linter that supports plain text, markup and source code comments.

Alternatively create a Regex presubmit check or filter to prevent certain typos or ambiguous terminology being including in code comments or content.

### 4\. Raise bugs

If you’re the first technical or UX writer in a company, raising bugs against spelling or grammatical issues in the product or the code is a good way to raise awareness about documentation and the skills you bring to the table.

![](/images/How-to-build-a-documentation-culture/0*Uq8fuKmllV5dzDdM.png)

When I joined a startup, I was initially nervous about raising bugs but after a few months of highlighting things like spelling issues, passive voice and typos, more and more engineers started coming to me for advice about content such as error messages, release notes, parameter names and code comments so we were able to ensure the text was correct in the first place.

### 5\. Reward writing

While it might sound cynical, offering engineers rewards or incentives for contributing to the documentation does work.

![](/images/How-to-build-a-documentation-culture/1*gt-KqiN5WDv5N3AeQErQAw.jpeg)

<figcaption>Stickers from the Write the Docs conference in Portland&nbsp;2018.</figcaption>

Some things you might consider include:

*   Running a doc-a-thon and offering prizes to the people who contribute the most documentation changes.
*   If your company runs a peer bonus scheme, give contributors peer bonus points for their documentation efforts.
*   Offer physical rewards or swag for contributions to docs such as stickers or mugs.

As a naive junior technical writer, I even had some success with handing out chocolate bars but I’m not sure this is the healthiest option for your colleagues or your wallet!

### 6\. Offer documentation training

If you’re a solo technical writer with a large team of developers, you can’t realistically be expected to write everything. Your best bet is to teach your team some documentation best practices to improve the quality of your docs.

Some topics you might want to cover include:

*   **Voice**: Using active voice instead of passive voice. The latter can create ambiguity.
*   **Ambiguity**: Avoiding the use of words that can create ambiguity. For example, an action is mandatory use ‘you must do x’ instead of ‘you should do x’.
*   **Audience**: Encourage your team to think about who they are writing for and any prerequisite knowledge or tools they might need.

### 7\. Give talks about documentation

I used to be terrified of public speaking but over the past two years, I’ve given a number of internal and external talks about documentation and best practices.

![](/images/How-to-build-a-documentation-culture/0*v1FSoFZtcUPKHp87.jpg)

<figcaption>Photo by <a href="https://unsplash.com/@xteemu?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" data-href="https://unsplash.com/@xteemu?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Teemu Paananen</a> on&nbsp;<a href="https://unsplash.com/search/photos/public-speaking?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" data-href="https://unsplash.com/search/photos/public-speaking?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Unsplash</a></figcaption>

It’s not only been a great way to test yourself and overcome your fears (if you’re not a comfortable public speaker) but it also helped to raise awareness about the importance of technical documentation both at your company and in the wider community.

### 8\. Use the open source community

If it fits with your business model or your product is open source, you can reach out to technical writers and documentarians in the open source community to help with your documentation.

![](/images/How-to-build-a-documentation-culture/0*zpVZhPEY8IYM3Voa.jpg)

<figcaption>Photo by <a href="https://unsplash.com/@perrygrone?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" data-href="https://unsplash.com/@perrygrone?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Perry Grone</a> on&nbsp;<a href="https://unsplash.com/search/photos/volunteer?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" data-href="https://unsplash.com/search/photos/volunteer?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Unsplash</a></figcaption>

Some companies like Google run open source initiatives where they actually pay technical writers to contribute to open source projects. See [Season of Docs](https://developers.google.com/season-of-docs/) for more details.

### Summary

So in summary, if you want to get started and build some form of documentation culture and improve your company’s technical content:

1.  Find a writer or “documentarian” to drive the docs.
2.  Create or choose a style guide to establish consistency.
3.  Use spell checkers or linters to establish quality.
4.  Raise bugs to raise documentation awareness.
5.  Reward writing to encourage others to contribute.
6.  Offer training to empower your colleagues.
7.  Give talks to inspire and teach others about docs.
8.  Use open source if you need more help!

There are probably lots of other things you can try but if you attempt some of these suggestions, I think you’ll be on your way to creating a documentation culture at your company. Good luck!
