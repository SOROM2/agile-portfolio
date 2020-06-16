---
layout: sprint
title: Six
order: 6
---

# Achievements

This sprint was a tiny workload, meaning myself and my teammates had a little time to work on other classes, I would consider this sprint a semi-break, or a break like sprint of some kind.

___

In this sprint I was assigned and completed the following tasks:

## Email notification for lack of site usage

This was covered over multiple sprints and completed in this one, this can also be seen in [the previous sprint](/five.html#email-notification-for-lack-of-site-usage) in its entirety.

![Issue 32](/img/32_issue.jpg)

This one required a bit of research as it was something completely new to anything I had implemented so far.

I had to create a Laravel Notification, which builds the email template by calling a set of MailMessage functions.

I also had to add a field to the users table in the database which would contain the last time an item was entered into a user profile. This field would have to be updated on every call of the 'store' method in the FormController.

Finally a schedule had to be added to the project that would check all the user profiles every day at a certain time, and a cron entry had to be added for the laravel scheduler on the server backend so that this would actually run.

Evidence of task:

![Evidence of profile for 9](/img/32_evidence.jpg)

## Go to display page of just entered data

![Issue 38](/img/38_issue.jpg)

This was as simple as adding a link to the tables page on the success notification for data form submissions.

Evidence of completed task:

![Input evidence for issue 38](/img/38_evidence.jpg)

___

# Self Reflection

## What did I do well?

Research of new features, same as previous sprint.

## What could I have done better?

Allocate myself more work, the workload was too light since the email notification task spanned 2 sprints.

## What lessons did I learn?

I learned speculation of how hard a task will be can sometimes be very inaccurate, and that this should be taken into account when allocating tasks, or perhaps bugs should be allocated when sprint promises are completed early.

## What barriers did I encounter?

None.

