---
layout: post
title:  "TDD: Test-Driven Development"
date:   2022-04-13 15:33:12 +0200
categories: jekyll update
---

**Test-Driven Development (TDD)** is a very well known term in IT - and probably it should be 
spread to other industries due to its usefulness.

There is already a lot of information on the Internet about TDD, its usage (with examples) and 
how beneficial it is in the projects.

So why even bother to write about TDD these days? Well... although a lot of engineers know the term and 
claim to use it, or even say a lot of good words about it... in practice they do not use this
"tool" in their craft at all.
This may sound weird, but that is the reality! I've been in so many projects where I heard how 
tests (and testing in general) are important. That we should be really testing our code, instead of
delivering features, waiting for bugs and fixing them if any appear.

Think about your project? How often have you heard something like: 
__"I finished implementation. Now I am adding some tests"__ - sounds familiar? ;-)

I've heard this statement in every single project I joined. The same old story... believe me, no exceptions!

In my first project as a Java Developer I was really confused about this whole situation. I would 
even say that it shocked me! Why? 
Imagine a Quality Engineer who spend last 3-5 years testing software, now joining new project as a 
Java Developer... I had my expectations... I hopped to see an attitude to catch issues as quickly 
as possible - next to the implementation - in unit tests. You know, the pyramid of testing that every QA can
recite at any time even at night.

Instead, I found out that in DEVS team:
* testing is postponed until development is completed (waterfall approach)
* tests are not written because estimates included implementation only
* developers do not have much knowledge about testing
* it felt like developers treated writing tests as some kind of punishment ;-)

In summary, it seemed like testing as a skill or a tool for building good software was always neglected by devs I knew.
This was sad as I understood why in my previous role as a QA I had a lot of work and why other QAs
were always suspicious about DEVS and didn't talk about some of them politely... it was always hard to 
build a good communication bridge between QAs and DEVs.

I remember my first "battle on words" about TDD and testing in general with one of Senior Developers. 
I tried to convince him that testing is very crucial and if done at the right time (before implementation) 
can:
* speed up development of the feature
* has less effort and cost 
* contributes to cleaner code 

He on the other hand claimed that:
* it is a waste of time for simple implementations
* it should be done after implementation

It was hard for me, back then as a fresh Java Developer, to change his thinking... so I had to agree on something
that he said - otherwise our relation in the team would be poor - so I said that writing tests especially in TDD
way (in first place) does not make sens when doing quick prototyping - spikes.

Years went on, I joined new projects where I noticed similar attitude among DEVS. 
But this time I did not care about it. I wanted to find out on my own what is the best way to write software.
I started experimenting and comparing implementations done using TDD with the one 
that had tests added after code was finished... and even with code that did not have tests at all.

I noticed following:



{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].


## References

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
