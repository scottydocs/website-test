---
title: >-
  GraphQL: “If there’s no documentation, people aren’t going to be able to use
  it…”
date: '2018-12-05T14:07:44.109Z'
excerpt: >-
  I recently gave a talk at the API the Docs conference in London where I was
  finally able to share some valuable advice about GraphQL…
thumb_img_path: >-
  images/GraphQL---If-there-s-no-documentation--people-aren-t-going-to-be-able-to-use-it/1*aNktTtMPA5TIzaB4NW_w-w.png
layout: post
---
I recently gave a talk at the [API the Docs](https://apithedocs.org/london2018) conference in London where I was finally able to share some valuable advice about GraphQL documentation. My talk followed my journey from first being told that GraphQL was self-documenting and didn’t need documentation, to [speaking to](http://documenter.co.uk/2018/10/10/the-origins-of-graphql-an-interview-with-lee-byron/) GraphQL co-creator Lee Byron in my quest for answers and receiving the words of wisdom that I was able to share at the conference.

![](/images/GraphQL---If-there-s-no-documentation--people-aren-t-going-to-be-able-to-use-it/1*aNktTtMPA5TIzaB4NW_w-w.png)

<figcaption>Me (left) at the start of my GraphQL&nbsp;journey…</figcaption>

After initially being told by a developer that GraphQL wouldn’t need documentation, I was pretty sceptical, but as I starting researching I found numerous examples of developers advocating GraphQL’s self-documenting nature with someone even declaring that it didn’t need documentation.

Although the majority of people were fairly positive about the self-descriptive features, I found some evidence including this tweet by a developer unhappy with GraphQL documentation he had encountered that made me realise I might be onto something:

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/MartinMikusat/status/1018855120572907521"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### 🤖 What does “self-documenting” mean?

I explored self-documenting actually means and from the definitions I found, in essence we’re talking about something that is written or structured in such a way that it can be understood without prior knowledge or documentation. However, I thought it was pretty interesting that the [PC Magazine definition](https://www.pcmag.com/encyclopedia/term/51077/self-documenting-code) came with this caveat:

> *“It’s very subjective. However, what one programmer thinks is self- documenting may truly be indecipherable to another.”*

![](/images/GraphQL---If-there-s-no-documentation--people-aren-t-going-to-be-able-to-use-it/1*eiotgPYVX6MJ_evHOZCFmQ.jpeg)

<figcaption>Cartoon from <a href="http://geek-and-poke.com/geekandpoke/2008/2/4/the-art-of-programing.html" data-href="http://geek-and-poke.com/geekandpoke/2008/2/4/the-art-of-programing.html" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">Geek and&nbsp;Poke</a>.</figcaption>

I investigated the risks of subjectivity, how words like homographs such as “second”, “number” and “subject” can have multiple meanings and might be interpreted differently. I also shared different opinions on self-documenting code, how some people feel it is a myth and an excuse for developers to avoid writing documentation:

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/slicknet/status/3559283285"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

I discovered a great [blog post](https://www.ericholscher.com/blog/2017/jan/27/code-is-self-documenting/) by Eric Holscher, one of the co-founder of [Write the Docs](https://www.writethedocs.org/), who wrote that self-documenting code was “one of the biggest documentation myths in the software industry” and argued that people who believe in a world of self-documenting code are actually making it more difficult for normal people to use their software.

He felt self-documenting argument boils down to three points:

*   I made something with a specific use.
*   I gave it a name to represent that specific use.
*   It doesn’t need documentation now because it’s obvious how it works.

### 🔬 How intuitive is GraphQL without docs?

To test some of these self-documenting claims, I decided to conduct a little experiment and stripped out the introductory documentation, including the query example, from the Github GraphiQL explorer. Then I challenged six of my colleagues, members of QA, development and documentation, to try and formulate a GraphQL query to retrieve my full name, location and avatar URL if I just gave them my Github login name.

![](/images/GraphQL---If-there-s-no-documentation--people-aren-t-going-to-be-able-to-use-it/1*X73R7dBuEte6WRQrbH__6w.png)

<figcaption>How GraphiQL (pronounced “graphical”) appears with no introductory text or example&nbsp;queries…</figcaption>

The results were pretty interesting with pretty much all of them struggling with the syntax and encountering fairly similar parsing errors. The amount of time it took them to formulate a query through trial and error proved to me that GraphQL isn’t actually that intuitive for a beginner without some form of example query or hand-holding documentation to get you started.

The other common issue I have encountered with some GraphQL APIs is people either failing to add descriptions or using ‘self-descriptive’ as a description for queries and fields that weren’t particularly descriptive. Some of these rely on assumed knowledge, expecting the end user to have a prior knowledge of the schema and the data it relates to.

When I searched the [GraphQL spec](https://facebook.github.io/graphql/June2018/), I found this line, which might explain why some developers are not including descriptions or have chosen to just write “self-descriptive”:

> *“All GraphQL types, fields, arguments and other definitions which can be described should provide a description unless they are considered self descriptive.”*

Whether they realise it or not, the issue is these people are unintentionally making it difficult for people to use their APIs. GraphQL co-creator Lee Byron [spoke about the importance of naming](https://www.youtube.com/watch?v=zVNrqo9XGOs#t=10m40s) at the GraphQL Summit in 2016:

![](/images/GraphQL---If-there-s-no-documentation--people-aren-t-going-to-be-able-to-use-it/1*r-bja7CITtIJVGbGjlwJEg.jpeg)

<figcaption>GraphQL co-creator Lee Byron spoke about the importance of naming at the GraphQL Summit in&nbsp;2016.</figcaption>

> “It’s really important not just to have names that are good but to have names that are self-documenting \[…\] Naming things that adhere closely to what those things actually do is really important to make this experience actually work.”

### 🐴 Straight from the horse’s mouth

I thought this was pretty interesting but I still wanted a definitive answer about GraphQL documentation, so emailed Lee, who is also the editor of the GraphQL spec, to see if he would answer some of my questions for a blog. To my surprise he agreed to a video call during which told me all about the history of GraphQL and his hopes for its development. When I asked him about the importance of descriptions in GraphQL, he said the following:

> “APIs are a design problem, way more than they’re a technical problem and you know this better than anybody else if you’re working on documentation. If there’s no documentation, it doesn’t matter how good the API is because so much about what makes an API work well is mapping well to your internal mental model for how something works and then helping explain those linkages and the details. If you do that wrong, it doesn’t matter how good your API is, people aren’t going to be able to use it…”

> “…GraphQL doesn’t do that for you, it provides some clear space for you to do that. There’s the types and the fields and introspection, you can add descriptions in places so it wants to help you but if you don’t put in the thought and you end up with a poorly designed API, that’s not necessarily GraphQL’s fault right?”

### ✍️ So how do we document GraphQL?

Lee spoke about how GraphQL provides you with “clear space” for the documentation: the types, the fields, the descriptions and introspection. So by using self-descriptive names for the types and fields and by using good descriptions in your GraphQL schema, you make it a much more user-friendly experience for your end user. However, these descriptions will only get you so far because documentation generated dynamically from your schema is never going to be very human.

Former technical writer and developer Carolyn Stransky [spoke about this](https://www.youtube.com/watch?v=FsRSdGuj588#t=6m42s) issue and a number of other blockers she encountered while trying to learn GraphQL at the GraphQL Finland conference. These included “an unhealthy reliance on the self-documenting aspects of GraphQL”, unexplained jargon and assumed knowledge. She felt most of these issues could have been easily prevented if more care and consideration had gone into the documentation.

Other technical writers have said similar. Andrew Johnston, who works on the GraphQL documentation at Shopify, [spoke about](https://www.youtube.com/watch?v=uuzsEfLaGnU&feature=youtu.be) the importance of providing on-boarding or “hand-holding” documentation for people who are new to GraphQL and not just assuming your end users will know how to formulate queries and mutations.

Meanwhile, in technical writer Chris Ward’s [blog post](https://blog.codeship.com/documenting-graphql/) about whether GraphQL reduced the need for documentation, he concluded that while it “offers a lot of positives on the documentation front”, documentarians should treat it just like any other API. He wrote:

> *“Documenting API endpoints explains how individual tools work, explaining how to use those tools together is a whole other area of documentation effort. This means there is still a need for documentation efforts in on-boarding, getting started guides, tutorials, and conceptual documentation.”*

The conclusion of my talk was that GraphQL can be self-documenting… but only if you put in the effort to use truly self-descriptive names, if you add adequate descriptions and if you provide sufficient supporting documentation, especially for people who are new to GraphQL.

Ultimately I think technical writers have a pretty important role to play in documenting GraphQL and ensuring the experience works for the end user, to repeat Lee Byron’s advice — if your API doesn’t have any documentation then people aren’t going to be able to use it.

**Further reading**: Here are my [slides](https://speakerdeck.com/scottydocs/is-graphql-really-self-documenting) and my [resources](https://gist.github.com/Jwscott22/c956c5328bca8e10cc8df9e3406104d7).
