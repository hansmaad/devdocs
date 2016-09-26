---
title: How we handle the Quality Assurance process
github_link: blog/_posts/2016-10-01-qa-at-speed.md
authors: [ms]
---

I often get questions about our development workflow at shopware. 
So I think it might be interesting to give you a little insight in our process.
 
As a software company, we try to cover the whole development process with in an agile culture.
Most of our teams are using Scrum or Kanban and we try to strictly follow the agile manifesto??? link
In an agile environment it is sometimes difficult to integrate the Quality Assurance(QA) process fluently.

In my carrier I was faced by many qa workflows. 
One of the worst idea was this approach: "We don't need extra testers. Tell the devs they can take more time developing and test things by themself but they have to stop creating bugs."

I think I don't need to explain why this statement was totally unworldly.
I am glad that this opinion has never existed in shopware. 
Like most of the development companies we had a separate testing department, but with this structure it seems as would a faster development process and good quality cancel each other out.
You might know the situation in which a lot of tickets stuck in the qa phase and the whole development process seems to stop.
But this is just one problem you will face when you have this kind of workflow.

A few months ago I came across an approach developed and used by Atlassian. 

[How to deliver quality assurance at speed](https://de.atlassian.com/agile/how-to-deliver-quality-assurance-at-speed-video/)

At first I was skeptical because the above mentioned sentence came to my mind.
But the more I thought about it the more it grows on me.
So I decided to present the idea to the team and I was surprised that nearly every one was totally into this approach.
The team agreed to give it a try.

At this point, if you have not already done, I suggest to have a look at the video cast from atlassian.

# Dotting
About a week later we started to work with the following workflow.

![](/blog/img/QAatSpeedPhase2.PNG)


In this scenario another developer will test the work of his colleagues.
After the code review a tester and a dev will meet and speak about the things the DOT(Developer on Test) need to test (Demo).

They speak about potential risks and define testing notes, which should always contain open questions instead of a list of click scenarios.

For example: What about the full page cache? What if we use https instead off http?

So the DOT can learn from the experience of the tester. The main reason for this procedure is to teach the DOTs how to test.
After the demo the DOTs start the actual testing.
Before each software release there is another testing phase done by the testers as a safety net and to analyse the testing quality of the DOTs.


## Problems
After a few days we faced a few problems which lead us to change the workflow again.

The problems were:  
* The selected developer for dotting were often the same colleagues. So the experience was unevenly distributed.
* Suddenly the new process was even slower than the process before, because a lot devs forgot about there dotting tasks or even postpone it. So many tickets stuck in this status.
* The author of a ticket didn't felt responsible for the quality.

# Our current workflow
After this experience we felt brave enough to go on with the last phase explained in the video.

![](/blog/img/QaAtSpeedFinalPhase.PNG)

Before the developer starts with a ticket. The QA and the dev meet for a QA Kickoff. In this short discussion they talk about risks or important things to think of while developing. So we can prevent any bugs before they exist.
After this discussion the developer starts to code and test at the same time. 

After the coding/testing the dev and the QA will do a normal demo like before. 
They speak about what the dev has tested and try to figure out missing scenarios.
The dev will test the missing scenarios by himself so he knows what to thing of next time.

The next step is the normal code review. Another dev will have a look at the code. When there is nothing to complain about the code will be merged and the ticket can be closed.
When the code reviewer discovers bigger structural problems, the dev needs to fix them and the process starts all over with the demo meeting.
 
Before every release the QA still performs a release test to make sure everything is fine.
About 5-8% of all tickets in the release still contain problems(rejection rate). 
It is very important to measure this value, because it is your only indicator to find out if the testing skills of your devs evolve.
By the way when we start our rejection rate was about 30-40%. 

So I think you can say that this approach worked very well for our situation.
In my opinion the best thing is that you nearly have no blocking qa status anymore. 
After the code review is done the ticket is done. 
This is the reason why it speeds up the development process massively.
It also scales perfectly with the number of developers which fits perfectly to a fast grown company.  
This is for sure not a general solution for every team or company but I think it is worth a try.
 
