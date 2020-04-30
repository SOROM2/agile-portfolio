---
layout: sprint
title: Three
order: 3
---

# Achievements

This sprint was far better than sprint 2, we managed to get 3 standup meetings into this sprint, which we think was really good but might have been a little too much seeing as we decided to shorten our sprints to 1 week to minimise procrastination and add a little time pressure as a motivator to get work done.

Another thing that went far better in this sprint was communication, both within the whole group and just between members that were having technical issues with their implementations of user stories.

![Example of back and forth communication between myself and a team member](/img/team_communication_example.jpg)

This sprint I decided to add an 'other' option to the gender selection fields, as I believe it would be more inclusive to any users of the site that don't identify as either Male or Female, so now members of the site have the ability to chose something other than 'Male' or 'Female', and they have the ability to change their gender at whatever time they want via the new profile edit page.

![New other gender options on the register page](/img/new_other_gender_option_register_page.jpg)

___

In this sprint I was assigned and completed the following tasks:

## Record Height

![Issue 41](/img/41_issue.jpg)

This was a little more difficult than I expected, I had to make a migration to add a heights table to the database, insertion code for the database, a form for inputs and a table for displays. The BMI calculation will be a part of a future user story.

In the future I would rate this type of task a 3 rather than a 2.

Evidence of input form:

![Input evidence for issue 41](/img/41_evidence_input.jpg)

And display table:

![Display evidence for issue 41](/img/41_evidence_tables.jpg)

## Customize what other people will see on my profile

![Issue 9](/img/9_issue.jpg)

This issue was about how I expected it to be, I added a bio to the profile page which meant I had to make a migration for the users database table to add it as a column, I added an edit page for profile and made the page autofill with the current info about the person.

I also added new web routes and extended the ProfileController.

The new profile page with a bio:

![Evidence of profile for 9](/img/9_evidence_profile.jpg)

The new profile edit page:

![Evidence of edit page for 9](/img/9_evidence_edit.jpg)


## Profile url uses 'name' instead of 'username'

![Issue 54](/img/54_issue.jpg)

This issue was very simple to solve, all I needed to do was to modify the existing web route and link in the nav bar from using $user->name (which is not unique) to using $user->username (which is unique)

The URL before the change:

![Evidence for before Issue 54](/img/54_evidence_before.jpg)

The URL after the change:

![Evidence for after Issue 54](/img/54_evidence_after.jpg)

___

# Agile

Since I have't talked about how my development and deployment environment has helped me be more agile yet in the portfolio, I will outline that here.

## The server

The server I do my development on is one that I self-host on my home network. Its original purpose was so that I could have something to ssh into when outside of my home network for the same development experience everywhere I go.

The server itself runs Arch Linux with the LTS kernel, this is because I wanted a minimal headless Linux installation with nothing initially running, so that if something runs on there, it's because I made it do that. This makes server-side problems far easier to troubleshoot and solve since I know what and how everything is configured.

![uname output](/img/uname_output.jpg)

Using Arch Linux may have a small barrier to entry because of the install process, but this results in benefits in the long term due to the rolling release nature of the distribution since updates are small and incremental, not large swooping changes that might break the site. This means I will spend less time on server maintenance and upkeep, and completely avoid critical distribution based errors.

The database I have chosen is MariaDB, which holds both the deployment database and the testing database, so that any migrations can be tested in an identical environment to deployment.

![MariaDB version output](/img/mariadb_version.jpg)

The web-server used is Nginx due to its simple configuration compared to Apache, which has been configured to use host-based routing so that I can specifically enable php only on the subdomains I need it and disable it everywhere else, such as in this portfolio which is hosted on the same server.

![test nginx configuration](/img/nginx_test_config.jpg)

## Development

I develop on the site exclusively using vim in tmux over ssh. This means no matter where I am, if I have one of my devices and an internet connection I can both develop on the site and administrate the server the same as if I were sitting right there at my desktop. This means if any issues arise with the server itself or the production environment, I can pretty much always access the server and quickly apply patches to the site or server software.

This makes the ability to be quickly flexible to changes regarding the server or site deployment very easy.

![Screenshot of development environment](/img/dev_environment.jpg)

I develop in the testing environment which has its own deployment of laravel, database credentials and subdomain so that the production and testing sites never interact or mix in any way. This means that if a git branch works as intended on the testing environment, it is guaranteed to work in the production environment as they both use the same versions of everything as well as run on the same web server, database and has the same system library versions and service configurations. This means the site can go from testing to production quicker, so the client will get their product quicker because no changes may need to happen since the deployment is tested on-server in the testing environment.

## Back to Agile

This whole setup allows myself, and by extension my team to spend less time messing with the server and its configuration, and more time on developing working software that can be almost immediately available to the client from the development->testing pipeline.

___

# Self Reflection

## What did I do well?

I communicated far more than before with my teammates than in any previous sprints. I also managed to help a teammate out with issues on their branch via slack.

Like every previous sprint, I have successfully completed my assigned tasks in time for the meeting with out client.

## What could I have done better?

I still procrastinated and didn't do any development work until the weekend, I need to start my work earlier in the week.

## What lessons did I learn?

I learned that even with the team size effectively cut in half, agile ensures the promised work will be completed regardless, this is what it means to be agile within a changing environment and changing scenario.

## What barriers did I encounter?

We currently have 2 team members that aren't participating in development of the project, this means I have to cover their user stories on the last day before our client meeting so we deliver on all of our promises to the client.

