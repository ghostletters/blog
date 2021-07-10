---
title: "The Higher Goods Require Sacrifices - From Others"
date: 2021-07-10T09:21:23+02:00
draft: false
tags: ["rant", "office", "politics", "orga"]
description: "Educate your team members. Waiting till 'they get it' is futile at best, or even malicious intent."
---

### Everybody Likes Nice Things

Most people can agree on a set of values and final results that they consider good and desirable. In case of software engineering terms like 'consistent design', 'maintainable code' or 'testable components' are fairly common and accepted as important goals. Only engineers out of their mind would argue for 'inconsistent design' or 'unmaintainable code'. However, the world is full of IT departments that pump out [Big Ball of Mud systems](https://en.wikipedia.org/wiki/Big_ball_of_mud) like if they hit an oil well. Wikipedia lists common reasons for such undesired results, for instance time pressure, high developer turnover or [software entropy](https://en.wikipedia.org/wiki/Software_entropy). So all the agreeable terms are good for nothing in the end? Not quite...

### We Do Politics - More Than Ever

Even so the term 'politics' is a slur for many software engineers, I would argue politics is unavoidable in any professional team setting. Even so hierarchies became flatter (at least when you look on the org chart) a team that wants to follow a shared vision or strategy will end up discussing different opinions and weigh opposing preferences. Some options will be mutually exclusive, others might have room for compromises. Finding and agreeing on one or the other means: we 'do politics'. The flatter hierarchies might have even fuelled the political debates, because it opened up room to 'bargain'. Where an almighty boss might 'just decide' which road to follow - in a team of equal partners there is room for discussions.

In political debates 'common grounds' are a valuable asset. Each party that can connect their position with the commonly accepted, 'good' values will have an advantage against the opposition. An example: lowering crime is a rather uncontroversial goal in society. That the police is somehow fighting against crime is also a believable stand. So one can frame an agenda that 'to lower crime we must increase the police head count '. Any opposition to this claim is in danger to look like they are against 'lowering crime', even so they just believe that other measures are more effective / have less side effects. Imagine the opposition would argue that more liberal abortion laws might be a better solution. This sounds rather unintuitive, right? Though, there is [quite some data](https://en.wikipedia.org/wiki/Legalized_abortion_and_crime_effect) that this is actually true.

### I Wish I Could - But I Don't Want

The same pattern can be applied in office politics. For instance, let's say that I am the pull-request-approval-guy in the team for historical reasons. When the team starts to grow multiple factors affect the review process

- new team members are not familiar with the code base and code style, so they are likely to introduce errors and inconsistencies. Very thorough review might be required
- the ratio of new 'code creators' and seasoned 'code reviewers' is getting out of balance. The increased number of reviews will increase the wait time for newly created pull requests
- both factors together (more thorough review + higher number of reviews) will compound the wait time

Fast reviews are one of the commonly accepted good things. Naturally, slow reviews are rather unpopular. So the new developers can rightfully complain about the slow approval process. Since the amount of new code should not be lowered (velocity!) the review capacity must be increased. However, I like the power and prestige that comes with being THE review guy and I feel no desire to share this glory. Of course I cannot argue that I think slow reviews are good. So I have to find another commonly accepted value to trump fast reviews. And this is where 'consistency' comes in handy. Obviously, a system created (or controlled) by 1 person is more likely to follow a consistent design than a system created by 10 persons (not necessarily a better system, but more uniformly).

So I will join the complaints of slow reviews, but unfortunately the higher good of consistency forces me to remain in power. I ensure everybody how much I dislike it, but my hands are bound. (You can add some crocodile tears here.)

### Wouldn't It Be Nice

This strategy is highly effective in practice. Everybody attacking the slow review process is now suspect of dismissing consistency. I can further strength my position by pointing out that consistency is valuable in the long run, while slow reviews are 'just a short term annoyance'. This argument is of course a strawman and rather convenient when all the 'short term' drawbacks hit someone else.

So what should we do instead? Just throw consistency out of the window for a bit of velocity gain in the short run? No, this approach was tested and market under terms like Extrem Programming. While there might be projects (and customers) where these approaches are suitable, for the average internal project I think their extremity is a liability.

So we _want_ to have a consistent system and thorough reviews _are_ an effective measure to ensure consistency. This means we need more people that are capable of conducting thorough reviews. Now the question is how do we get these reviewers? This is a critical question for me, the I-like-to-keep-review-power guy. One might tell me:

- reviews are a real problem currently. We should actively educate others to become reviewers. So we write down some code guides, document our architecture, collect and present common errors, organise pair programming, code katas and...

OR I tell the people

- after being reviewed _enough_ you will turn into a capable reviewer. Don't worry about when this will happen, I will tell you. Bonus, you don't have to actively do anything. Please also refrain from asking. Thanks a lot.

### Education as Explicit Goal

I believe you have to do things to get good at it. That also means that you start doing stuff while being bad at it. There is simply no way that a surgeon doing the first brain surgery is as good as we want a doctor to be. Nevertheless, s/he must jump into the cold water at some point and the only thing we can do about it is to place a seasoned surgeon next to the first timer. The problem cannot be fixed by watching a brain expert for years or by receiving a couple of brain surgeries. You have to fucking do it. And most likely you will suck in the beginning. Then someone else has to clean up the mess you produced.

And just to be clear - I am not advocating for the broken practice of 'training on the job'. Of course, you must provide a med students with a bunch of books before you allow them to touch a scalpel. Of course, you let them train on dead animals before allowing them to get close to a living human. Obviously, these things happened according to a plan and you are not hoping that they happened by chance, just because the student might have found a dead animal while stumbling over the right book.

Naming any learning material or even going the extra mile and structuring the learning process into an ordered list of actions, seems like an impossible endeavour for some software engineers. Everything is sooo complex, sooo highly dependent (unclear on what, but certainly highly dependent on _something_) that writing it down or even talking about it beyond meta physics is impossible. It is even futile to try, like building a perpetuum mobile.

I say this is all sheer nonsense and mostly boils down to

> “It is difficult to get a man to understand something, when his salary depends on his not understanding it.”

{{<source "Upton Sinclair" "https://en.wikipedia.org/wiki/Upton_Sinclair">}}

So we engineers should tackle this problem like all the other difficulties we deal with on a daily basis. Sit down, break up the problem into smaller parts till they become actionable. Research which actions are available and applied by others. Try out different solutions and measure what works best. We do not hope for 'time will magically solve our problems'. THIS would be futile.