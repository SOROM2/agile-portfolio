---
layout: sprint
title: Four
order: 4
---

# Achievements

This sprint continued the goodness from sprint 3, the team was communicating more, and work was being done far earlier in the sprint compared to the first 2 sprints.

This to me is evidence that the one-week sprints are better for this specific team and that this should be a habit my team maintains. I will try my best to encourage my team in this regard.

___

In this sprint I was assigned and completed the following tasks:

## Users can arbitrarily edit other user's profile page

![Image of issue 64](/img/64_issue.jpg)

Before this fix, any user could access and successfully submit changes to any other user profile edit form.
All that was needed was an auth check on the form POST and a redirect after, as well as an inline auth check on profile page to decide if the link to the page should be displayed.

Before the fix:

![Evidence of task before](/img/64_evidence_before.jpg)

After the fix:

![Evidence of task after](/img/64_evidence_after.jpg)


## Start and current values on profile page 

![Image of issue 60](/img/60_issue.jpg)

This was relatively simple, all that was needed was to query the databse for this user's most recent weight and height, then format and display it on the page along with the initial data.

Evidence of task:

![Evidence of task before](/img/60_evidence.jpg)


## Gender label on register page

![Image of issue 61](/img/61_issue.jpg)

This was just a fix to the previous sprint where the gender label was missing on the form.

Evidence of task:

![Evidence of task after](/img/61_evidence.jpg)


## Image on profile page

![Image of issue 59](/img/59_issue.jpg)

This issue was very fun to implement and came with a few interesting security things to think about.

One of these was predictable file names, this was mitigated by using the current UNIX epoch time as a filename, to ensure that at any moment, any new files would have names that didn't clash with other user profile images.

Another one was potential for MIME types to be spoofed and have malicious files placed into the website filesystem.
This was partially mitigated by having a minimum image size so that basic php webshell file uploads would be rejected.
This was also tested for code execution, and a file containing php code could be uploaded to the server, but code couldn't be executed, meaning the file upload is relatively safe.

Evidence of task:

![Evidence of task after](/img/59_evidence.jpg)
![Evidence of file upload form](/img/59_evidence_form.jpg)

___

# Self Reflection

## What did I do well?

I think I dealt with the security of the site in a timely manner, as well as maintained contact with my team more.

## What could I have done better?

Get my teamates to properly analyze code in pull requests rather that immediately confirm the request.

## What lessons did I learn?

Security is a huge factor and it is easy to implement code that can be manipulated by an attacker in a way that is unintended.

## What barriers did I encounter?

I do not believe I encountered any identifiable barriers during this sprint.

