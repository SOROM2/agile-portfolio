---
layout: sprint
title: Five
order: 5
---

# Achievements

This sprint was about half the size of the last sprint was, while the last sprint's workload was maintainable, it was a bit much for the one-week sprints we allotted ourselves.

___

In this sprint I was assigned and completed the following tasks:

## Password Resets

![Issue 43](/img/43_issue.jpg)

Getting emails working seemed difficult at first, but the implementation was easy, so easy that laravel didn't require any code changes to get it working.

It turns out, the laravel auth package handles password resets by default, meaning all I had to do was make sure the right routes were being used, then configure the .env file with smtp credentials for an outlook account.

Evidence of password reset email:

![Input evidence for issue 43](/img/43_evidence.jpg)

## Email notification for lack of site usage

![Issue 32](/img/32_issue.jpg)

This one required a bit of research as it was something completely new to anything I had implemented so far.

I had to create a Laravel Notification, which builds the email template by calling a set of MailMessage functions.

I also had to add a field to the users table in the database which would contain the last time an item was entered into a user profile. This field would have to be updated on every call of the 'store' method in the FormController.

Finally a schedule had to be added to the project that would check all the user profiles every day at a certain time, and a cron entry had to be added for the laravel scheduler on the server backend so that this would actually run.

Evidence of task:

![Evidence of profile for 9](/img/32_evidence.jpg)

___

# Agile

I have nothing to say in terms of new things agile-related for this sprint, as it was essentially the same as the previous sprints, Myself and my team seem to have 'got into the groove' of remote agile development work.

Now that I adequately know the codebase and systems of the website, it seems trivial to work in sprints, hold standup meetings multiple times a sprint, meet up with the customer and present new features, and to regularly update the kanban board on github to accurately represent what is being worked on currently so that teammates can coordinate their development to avoid merge conflicts.

___

# Self Reflection

## What did I do well?

I researched the new features and successfully added them to the existing project without much of a hassle by reading the official documentations and following the guides there.

## What could I have done better?

Allocate more work, one of my tasks was a 10 minute job, and was far easier to do than I thought.

## What lessons did I learn?

I learnt that official documentation is the best source of information for a framework or API, and that I should rely heavier on that than sources like stackoverflow.

## What barriers did I encounter?

Initially finding what I needed in the documentations took me a few hours, I thought I would need to create an Email facade, but it turns out I actually needed to create a Notification and call it from a schedule.

