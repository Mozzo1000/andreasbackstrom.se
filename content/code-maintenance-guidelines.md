---
title: Open source maintenence guidelines
author: Andreas Backström
date: 2022-10-23
slug: open-source-maintenence-guidelines
---

I have worked on a lot of projects through out the years. Some projects made it to github, meaning I spent more than a day working on it but some never see the light of day. But most of them are unfinished pieces of work that have helped me learn programming and developing projects.

As of writing, I have 42 repositories on github. Out of these 42 I can maybe say that 2 of them are finished projects but finished does not neccesarily mean that I never touch the project again. Being finished still requires one to update and keep the code running. I have been notoriously bad with updating my projects and keeping them maintained. These set of guidelines are meant to help me (and others if they like) to keep projects that are important to oneself maintained.


## Guidelines
### 1. Set expectations
Setting expectations are not only importartant for others but also yourself. Expectations makes everyone understand what you get with a project and what will be done in the future. Will you be adding new features continously or will you only be updating dependencies to keep everything secure?


#### 1.1 Write in the readme
A great example of this is what <a href="https://github.com/ssddanbrown" target="_blank">Dan Brown</a> does in some of <a href="https://github.com/ssddanbrown/rss#low-maintenance-project" target="_blank">his projects</a>.

A clear paragraph describing the creators intentions with the project and using the clear wordings like "low maintenance" or "abandoned".  

#### 1.2 Use badges
Badges are a great way to symbolize your intent and status of the project. Put these at the top of a README document.

**Examples:** 

<img src="https://img.shields.io/badge/maintenance-updates%20only-informational"/>

```<img src="https://img.shields.io/badge/maintenance-updates%20only-informational"/>```

<img src="https://img.shields.io/badge/maintenance-not%20maintained-critical"/>

```<img src="https://img.shields.io/badge/maintenance-not%20maintained-critical"/>```

### 2. Automate as much as possible
You do not want to spend your free time with doing mundane, boring tasks. Automate as much as possible.
For example, use <a href="https://github.com/dependabot" target="_blank">dependabot</a> (or similar depencendy tool) to automatically notify you about updates that need to be made to your projects.

#### 2.1 Things to consider automating
- Outdated dependency notifying
- Deploy on push. 
  - When pushing to github, have your production or testing server automatically update.

### 3. Archive old projects
If you have old projects that you have no intention of ever updating or using again, archive it.

With Github you can use the <a href="https://docs.github.com/en/repositories/archiving-a-github-repository/archiving-repositories" target="_blanl">archive features</a>. Remember to make the last changes before archiving. This can be change some badges or description indicating that the project is no longer maintained.

### 4. Add a license
A license will help anyone else understand what they can do with your project. If you are no longer maintaining a project and you have no license no one else can pickup the project and move it forward. 

If you want somebody else to be able to work on your project, add  an appropriate license.

### 5. Pin your dependencies
It is frustrating having to deal with breaking changes in your dependencies when needing to use a project on a new machine. Having not worked with the code in a while adds to the frustration as you may not be familiar enoguh in order to quickly fix the issue. 

This is why you should pin all your dependencies to the exact version that you know your project works with. This will require you to update the versions from time to time but in the long run your project will still work the same way as intended. 

<hr>
## Maintenance status specification DRAFT
*This is a draft of an idea of having a specification indicating a projects current status. I may or may not elaborate further on this idea in the future.*

### Status

#### Under development
The maintainer is activly adding new features and updating the project.

#### Updates only
The maintainer will only be updating dependencies. No new features or bug fixes will be made.

#### Not maintained
The maintainer will not be updating dependencies, add new features or fix any bugs in the project.
<hr>
## Summary
These guidelinesare in no way set in stone, these ideas are all a work in progress and will need to be tested in the real world.

Moving forward, I will be utilizing these guidelines in all my projects and try and update existing projects that I do use in production.