---
title: How to write the perfect error message
date: '2019-02-12T06:01:01.039Z'
excerpt: >-
  Error messages are seemingly so innocuous but they’re actually incredibly
  important in ensuring good UX and keeping your end user happy. A…
thumb_img_path: images/How-to-write-the-perfect-error-message/1*oIAOgEBbTfFSIRSpwbXa3Q.png
layout: post
---
![](/images/How-to-write-the-perfect-error-message/1*oIAOgEBbTfFSIRSpwbXa3Q.png)

Error messages are seemingly so innocuous but they’re actually incredibly important in ensuring good UX and keeping your end user happy. A good error message informs your customers what went wrong, why it went wrong and what they can do to resolve it. Microsoft’s Windows [developer centre guidelines](https://docs.microsoft.com/en-us/windows/desktop/uxguide/mess-error) give the following advice:

> “Effective error messages inform users that a problem occurred, explain why it happened, and provide a solution so users can fix the problem. Users should either perform an action or change their behavior as the result of an error message.”

If you get that wrong, it can not only lead to frustration and low product satisfaction but in the worst cases you might lose credibility with your customers or end up being ridiculed on social media.

Although getting error messages right isn’t always easy, there are simple steps to follow to ensure you don’t leave your end users in the dark (or rolling around on the floor in fits of laughter).

### Check your spelling and grammar

Accurate spelling and grammar are vital for ensuring your audience understands the message you’re trying to get across. The professional quality of your external facing content also reflects the professional quality of your product and your brand.

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/sarambsimon/status/588761884087685120"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Although spelling mistakes and typos can sometimes be quite harmless and funny, if your content lacks accuracy, you also run the risk of causing confusion. If you’re not confident about your choice of wording, ask a technical writer or content specialist for help.

### Be specific

Default error messages like “There has been an error” or “An error has occurred” are really unhelpful. Don’t just tell your end users that something happened, tell them why it happened and what they can do to fix it.

Dubbed as “[the least helpful error in Windows history](https://www.wired.co.uk/article/windows-10-something-happened-error)”, Microsoft presented users with an error message that simply stated “Something happened” when they tried to install Windows 10:

![](/images/How-to-write-the-perfect-error-message/1*Rjh0ZDqJIz5vPaJguQ_kAA.jpeg)

<figcaption>Ahh something happened…</figcaption>

This error message was so bad it became something of a social media meme with users ridiculing how unhelpful it was. The solution, which was revealed by someone on [Reddit](https://www.reddit.com/r/Windows10/comments/3ezp5j/something_happened_during_my_windows_10/), was as simple as changing your language settings but the text was so ambiguous it could have remained a total mystery.

### Provide the right amount of detail

If you can explain what has gone wrong, then add a description in non-technical terms so your user understands the context. It’s great to be polite but simply posting an error message saying “Sorry” or “Oops” doesn’t really help anyone.

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/SteveBMorgan/status/858603279730737152"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<figcaption>You should be sorry.</figcaption>

If you’re going to say “sorry”, follow it up with an explanation of what happened and offer some actionable steps so the user can resolve the problem.

### **Avoid jargon and developer speak**

Remember that you aren’t talking to another developer. Your end user doesn’t read code or care about the internal processes involved in making your product work. Break down what’s going on in simple terms that anyone could understand.

In this example where the user was trying to create a new password, the validation error message text is overcomplicated and contains developer jargon.

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/daddyiwantapony/status/850157831713988608"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

It would have been much better to say something like: `Please try again. Your password needs to contain both lower and upper case characters and a special character`.

Another example of bad developer jargon appears in the [Microsoft dev center guidelines](https://docs.microsoft.com/en-us/windows/desktop/uxguide/mess-error) under the heading “incomprehensible error message”:

![](/images/How-to-write-the-perfect-error-message/1*AksrpJ0g1XOeUMIffwXytg.png)

<figcaption>Don’t be a robot&nbsp;🤖</figcaption>

What’s an MM error? What’s a standard FsRtl filter? What does this 0xC00000EA code mean? This error message might explain the problem from a developer’s perspective but it will leave most users with more questions than answers.

### Be human and friendly

While you’re thinking about how to avoid using jargon and developer speak, it’s also good to remember to be human. Your end users don’t want to feel like they’re being spoken to by a robot. Remember to speak their language and be friendly in your messaging.

This error message from the Meta Stack Exchange site is a good example of how you can be human and friendly in your messaging:

![](/images/How-to-write-the-perfect-error-message/1*fzkqz8kh8OGnMYZq6FDKAQ.png)

<figcaption>“It’s not you, it’s&nbsp;us…”</figcaption>

Sure, it isn’t particularly specific and it’s rather lengthy but it is apologetic, it makes it clear the error wasn’t your fault and informs you that the error has been recorded and will be investigated.

### Be clear and unambiguous

Ambiguity doesn’t help anyone. Presenting your users with some vague message that offers no practical information about what is going on and what users can do to solve the problem is really unhelpful.

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/grantmccall/status/1016837913026297856"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

If your error message is confusing, it has failed its primary objective. Think about what you are trying to tell the end user, how they will process that information and present it in the clearest possible terms.

If you’re unsure, get a tester or someone in a non-technical department to read the text and see if they can make sense of it.

### Be concise

Users don’t want to read your life story in an error message. If something has failed, an error message should be a short, concise piece of text that tells them what went wrong and provides a potential resolution to the problem.

![](/images/How-to-write-the-perfect-error-message/1*UmlC1k5z_h_Dcn4dsOEGwQ.png)

<figcaption>So much&nbsp;text!</figcaption>

[Research by the American Press Institute](http://prsay.prsa.org/2009/01/14/how-to-make-your-copy-more-readable-make-sentences-shorter/) found evidence that shorter sentences resulted in greater understanding:

*   For sentences that were 8 words or less, readers understood 100% of the information.
*   For sentences that were 14 words long, readers understood 90%.
*   For sentences that were 43 words or longer, comprehension dropped to less than 10%.

On that basis, there is an argument for keeping your sentences short. Author Martin Cutts makes the following recommendation in the [Oxford Guide To Plain English](https://read.amazon.co.uk/kp/embed?asin=B00FZSX76G&preview=newtab&linkCode=kpe&ref_=cm_sw_r_kb_dp_aFkyCbSKPGCZN):

> “…make the average sentence length 15–20 words…More people fear snakes than full stops, so they recoil when a long sentence comes hissing across the page.”

### Voice and tone

Choosing the right voice and tone for your error messages is really important. You shouldn’t use an accusatory tone that makes the user feel like they’ve done something wrong or that the error was their fault:

![](/images/How-to-write-the-perfect-error-message/1*Gbu2UBItAIqBLr0u6aLt5g.png)

<figcaption>Don’t make your user feel like a criminal!</figcaption>

You might want to consider ensuring the tone you use is in keeping with your brand. Slack is known for being quite playful with their messaging:

![](/images/How-to-write-the-perfect-error-message/1*elXajeLoCVaxECVlWdUQ5g.png)

Anna Pickard, Slack’s head of brand communications, [said](https://www.contagious.com/news-and-views/slacks-editorial-soul-anna-pickard-on-writing-the-brand-experience) the friendly and sometimes playful tone of the editorial copy was intended to make users feel like they’re talking to a friendly co-worker:

> “It is sometimes funny, sometimes serious, sometimes just plain and informative, but throughout, it should feel like nothing more than a person, talking to another person. Human to human.”

[Apple’s Human Interface guidelines](https://developer.apple.com/design/human-interface-guidelines/macos/windows-and-views/alerts/) advise using a friendly tone helps to avoid sounding accusatory or judgemental:

> “People know that alerts notify them about problems and dangerous situations. As long as you use a friendly tone, it’s better to be negative and direct than positive and oblique.”

### Add humour when appropriate

Having a sense of humour is good but sometimes trying to be funny can fall short of the mark if your error message isn’t particularly helpful:

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/ShedworksGreg/status/801048908017188864"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<figcaption>Looks like Slack changed <a href="https://slack.com/404" data-href="https://slack.com/404" class="markup--anchor markup--figure-anchor" rel="noopener" target="_blank">this error</a> since and added a link to their help centre.</figcaption>

Github’s 404 page mimicking Obi-Wan Kenobi’s [famous quote](http://www.youtube.com/watch?v=532j-186xEQ&t=0m44s) from Star Wars is a nice example of combining humour and knowing their audience:

![](/images/How-to-write-the-perfect-error-message/1*7GRNR2xZJjEpMiDBoDVQ7g.gif)

In [Mailchimp’s content style guide](https://styleguide.mailchimp.com/) they recommend only trying to be funny when it comes naturally and not forcing it when it’s inappropriate:

> “…feel free to be funny when it’s appropriate and when it comes naturally to you. But don’t go out of your way to make a joke — forced humor can be worse than none at all. If you’re unsure, keep a straight face.”

### Think about colour and design

It is important to think about the colour and design of your error messages so they are UX friendly and accessible to all of your users’ needs. Don’t choose colours for your font and background that are too similar or will be difficult for people with colour blindness to distinguish between:

![](/images/How-to-write-the-perfect-error-message/1*Fq4qhwwOYbk4Qm6H8SMYzQ.png)

<figcaption>Don’t use colours that clash or would be difficult for people with colour blindness to&nbsp;read.</figcaption>

Some general guidelines to follow are:

*   Avoid using font and background colours that clash.
*   Think about accessibility. Users with colour-blindness might not be able to distinguish between shades of red and green. Do not rely on colour alone to convey the meaning of the message, use icons or symbols as well. For example, ‘!’ for warning, ‘x’ for error.
*   Be consistent if you are going to use colours to denote different types of alert. For example, green for a success message, yellow/orange for transient warnings and red for an error message.
*   Choose a font and background colour that contrast nicely.

Red is probably the most common choice for error messages and associated icons. [Research](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4383146/) on colour psychology by professor Andrew J Elliot found that people’s attention was drawn to the colour red much faster than other colours:

> “In research on color and selective attention, red stimuli have been shown to receive an attentional advantage… Participants’ visual search times were faster for desaturated red (relative to several other colored) targets”

In [his paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.438.157&rep=rep1&type=pdf) about colour associations, psychology professor Dr Arlen C. Moller noted how red usually conveyed negative information in everyday life (e.g. alarms, traffic lights and financial statements) and had objective connotations with danger in the form of fire and blood. So people do use the colour red for good reason!

### Summary

In summary, when creating your next error message remember to think about the following things:

1.  Spelling and grammar. Accuracy is important.
2.  Be specific. What happened?
3.  Provide the right amount of detail.
4.  Avoid jargon and developer speak.
5.  Be human and friendly.
6.  Be clear and unambiguous.
7.  Be concise. If in doubt, aim for 15–20 words per sentence.
8.  Choose the right voice and tone.
9.  Add humour but only when appropriate.
10.  Think about colour and design.

**TL;DR —** Write your error messages in concise, friendly and non-technical language that everyone can understand. Otherwise they’re pretty useless.

### Resources:

1.  Microsoft Windows Dev Center guidelines on Error Messages: [https://docs.microsoft.com/en-us/windows/desktop/uxguide/mess-error](https://docs.microsoft.com/en-us/windows/desktop/uxguide/mess-error)
2.  “Windows 10’s ‘Something Happened’ error is turning into a meme”, WIRED article: [https://www.wired.co.uk/article/windows-10-something-happened-error](https://www.wired.co.uk/article/windows-10-something-happened-error)
3.  How to make your copy more readable: Make sentences shorter: [http://prsay.prsa.org/2009/01/14/how-to-make-your-copy-more-readable-make-sentences-shorter/](http://prsay.prsa.org/2009/01/14/how-to-make-your-copy-more-readable-make-sentences-shorter/)
4.  Slack’s Editorial Soul: Anna Pickard on writing the brand experience: [https://www.contagious.com/news-and-views/slacks-editorial-soul-anna-pickard-on-writing-the-brand-experience](https://www.contagious.com/news-and-views/slacks-editorial-soul-anna-pickard-on-writing-the-brand-experience)
5.  Apple’s Human Interface Guidelines on Alerts: [https://developer.apple.com/design/human-interface-guidelines/macos/windows-and-views/alerts/](https://developer.apple.com/design/human-interface-guidelines/macos/windows-and-views/alerts/)
6.  Voice and Tone: Mailchimp Content Style Guide: [https://styleguide.mailchimp.com/voice-and-tone/](https://styleguide.mailchimp.com/voice-and-tone/)
7.  Basic Hue Meaning Associations: Arlen C. Moller: [http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.438.157&rep=rep1&type=pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.438.157&rep=rep1&type=pdf)
8.  Color and psychological functioning: a review of theoretical and empirical work: [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4383146/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4383146/)

* * *
