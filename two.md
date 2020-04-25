---
layout: sprint
title: Two
order: 2
---

# Achievements

This sprint wasn't as good as the previous.

This sprint lasted for 4 weeks due to many factors that will be more thoroughly covered further down.

As a group we went through and ranked different tasks on a logarithmic spectrum of 1-10 in difficulty, where 1 is the lowest value, and 10 is as difficult as a task could possibly be.
This will help us in the future sprints when dealing out tasks for members of the group to complete.

It is apparent from the usage of our slack channel we are communicating more and that we as a group are putting more effort into communication with each other and the client.

___

In this sprint I was assigned and completed the following tasks:

## Redirect / to /home if logged in

![Issue 44](/img/44_issue.jpg)

This was another relatively trivial feature to implement, All I needed to do was make a check in the web routes if the page visitor is logged in, if so redirect them to /home else return the welcome view.

![Evidence for Issue 44](/img/44_evidence.jpg)

## Log in with username

![Issue 33](/img/33_issue.jpg)

This was far more difficult than I initially thought it would be.

Not only did I have to add a database migration to add a username field, on the registry form and the login form, but I also had to use the object orientedness of PHP in order to override the 'credentials' from the 'Auth\AuthenticatesUsers' class to check for both fields.

I also had to add login and registry errors to the form, modify the User.php class to include 'username' as a fillable field, and also add some lines to the RegisterController to actually populate the username field from the login form input.

This is the register form before the change:

![Register evidence before for Issue 33](/img/33_evidence_register_before.png)

And the login and register forms after the change:

![Login evidence after for Issue 33](/img/33_evidence_login_after.jpg)
![Register evidence after for Issue 33](/img/33_evidence_register_after.jpg)

___

# Agile
This sprint was very interesting and I think my attitude towards agile is warming up as I use it more.

This sprint was rather unique in terms of agile, because the New Zealand government initiated a full country lockdown. This meant myself and the team would have to adapt to the changing situation in the country, and almost completely change the style in which we worked as a group. Previously we worked partly remote from home and partly at polytech, but due to this lockdown, we have been forced to work completely remotely.

There is no doubt this impacted out performance, and it is visible on out kanban board for sprint 2.

At the closure of this sprint, it was agreed upon with out client and amongst the members of the group that we would reduce the duration of a sprint from 2 weeks to 1 week in the hope that it would reduce procrastination, increase communication between the members of the group and increase communication between the group and our client.

It was also agreed to add the client into the same group chat we use for communicating so the it would be both easier to get a hold of the client if we needed, and so the client could see what we are working on and monitor our progress easier. The client also has access to the github repo for the project for the same reason.

A way I demonstrated ability to adapt to quickly changing situation was just before the meeting with out client, where a team member mistakenly merged active bugs into the development branch which we were about to show the customer. So I went through, identified and patched the bug so that the product was in tact for the demo with the client.

The following pull requests are from that scenario:

![Last minute bug fix](/img/agile_quickfix_1.jpg)

Overall this sprint was a challenge when it came to agile, it threw our team into the deep end of being adaptable and malleable to changes in the project and changes in the world. While we may have flopped on this occasion, it serves as a valuable learning experience and a big reminder that we have a lot to learn about group collaboration, teamwork, leadership and preparedness to change on a dime.

___

# Self Reflection

## What did I do well?
I completed all of my tasks within a week of the start of the sprint and I put more effort into communication.

## What could I have done better?
Communication could still be better, I know both myself and my group find it difficult to do fully from-home remote work, so I need them to support me, and they need me to support them back.
Next sprint I will be putting far greater effort into communicaton with my group, as some of us didn't end up completing all of our work on time even given the extended time frame that we had to work in.

## What lessons did I learn?
Communication is quite literally the most important aspect of collaboration, I didn't really fully understand or agree with that statement until we were forced to be locked down into our own houses and forced to work in absolute isolation from my team. I also learned that some tasks can me more complex than they seem on the surface. I initially thought making the username-email login would be quite simple and that I could have it done in a few hours by creating a migration to add the username field to the database, just do 2 querys and check on the output of both queries, maybe if I was writing this in pure php that would be the way to go, but Laravel has its own way of handling stuff like this. As a result I spend more than just a few hours reading through the laravel documentation to get every aspect of the feature up to the proper standards of how Laravel works.

## What barriers did I encounter?
The lockdown due to the current virus outbreak has had a large hit on the morale and motivation of both myself and the team, getting used to this way of life and this way of remote collaboration has been difficult, but will hopefully get better and become easier as time goes on.

Another barrier was that a team member has recently been unable to participate in collaboration for external reasons unknown. I need to be able to adapt to these situations as they arise and quickly re-plot not only my own course, but be the one to take action and plot the course for the group in the future.

