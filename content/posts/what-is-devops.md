+++ 
draft = false
date = 2019-08-31T11:55:31+01:00
title = "What is DevOps?"
description = "Hint: it's about more than just knowing how to run Containers."
slug = "what-is-devops" 
tags = ["devops","storage","security"]
categories = []
externalLink = ""
series = []
+++

Put simply, it's a methodology to close the gap between Devs (Developers) and Ops (Operators) in IT Teams. Historically, Developers created Artifacts (Code, Binaries, ...) that Ops had to deliver to the customer (as a Software Package, a Webservice, ...). Ideally, Developers define the technical dependencies their Artifacts need to be run successfully and Ops takes care of the right environment, monitoring and so on. Traditionally, this is a back and forth between to irresistable forces and, at scale, imposes more problems than it solves.

That's why, at some point, Devs and Ops sat down to discuss how to better manage their relationship and came up with a new concept of handling workloads and IT processes: DevOps. 

## Fast Forward to 2019
Lately, DevOps seems to become a buzzword and almost a synonym for "Kubernetes", "AWS" and "Pipelines". Of course, there's more to it. DevOps is a methodology. It's a certain way to think and it's a special attitude and mentality one has when it comes to dealing with the unknown (aka "problems"). It certainly can't be limited to a subset of tools that only solves a subset of problems.

A DevOps Engineer is a Generalist. He knows enough about the Artifact **and** the Environment (Infrastructure) to be able to optmize both ends. That's why a DevOps Engineer is often associated with **Full Stack Developer**. Typically, a DevOps Engineer also has a deep expertise in one of the professions his role came from - Dev or Ops. So he might be a Senior Java Developer or a Senior Linux Sysadmin, either building super efficient Artifacts that can deal with commodity Infrastructure or building modest Code in a highly optimized Environment. Either way, both commit to the solution of a business problem while sharing a common way to think and work. So a team of multiple generalists with strong expertise coupled with a few single-scoped experts (Databases, Storage, Designers, ...) makes for a dynamic problem-solving machine.

To DevOps, there are 3 key principles that I think apply to the role, the engineer, his team and the system he's part of:

## 1. Everything is a system, even you
Just accept it. Systems help making things easier. Society is a system that helps us get along, a Job is a system with clear boundaries, input and output; you are a system of cells that writes Code.

A system is typically composed of other systems. And so on. So let's just assume you're a DevOps Engineer (a `Problem-Solving System`) in a SaaS Startup (another `Problem-Solving System`). You solve problems for the Startup so it can solve problems for its customers. Let's magically remove office politics, social networking and idiots from the Parent System (the `Startup`) and personal preferences from you (the `DevOps`) and assume, for a moment, both Systems can use their full capacity to solve their respective problems.

For both Systems, it is necessary to know what their purpose is to be able to `identify` the actual problems to solve. The Startup's Mission is to collect the latest Job-Offers for Developers in a certain area and deliver them to interested Developers looking for Jobs. For this, it needs to collect the Job-Offers and provide some kind of Subscription Service to their target audience (Developers). The `Startup` hires the `DevOps` Engineer to solve this problem. For the `DevOps`, the definition of problem probably looks slightly different:

- Do we need User Accounts?
- Database? Mongo or SQL? Hosted?
- Use a Framework?
- What language to write in?
- How to SSL?
- What about E-Mail?
- Cloud or on-premise?
- How to collect offers? Scraping? Manually? Submission?
- ...

There are a few things you need to know to solve the business problem - and maybe you can't deliver on all. So here's how a system works: as a good `DevOps` you identify the constraints of your own system in regards of the problems it needs to solve and then do 3 things: 

1. You optimize your System so it can optimize the Parent System (Learn Stuff)
2. You do this incremental and employ additional systems as needed to solve the overall problems (Get Help)
3. You always **implement** or **prepare for** `Automation` (Everything as Code)

This is an infinite cycle as you will see in `3`. Over time, you will incrementally describe your System and the Parent System and get better understanding of when, what and how to optimize. This helps on all ends. 

Now leaving Neverland, back to corporate real-world, where the Systems you're in are full of unrelated obstacles and theatre - where "doing as I want" is often superior to "solving the problem" - it's of course not that easy to ever get a glance at the bigger picture or a saying in how things will be done.

Yet, that's how in DevOps you should percieve your environment. Since the System you're dealing with is most likely an IT system and more and more things rely on these systems to work, the way you solve problems makes a huge difference for the whole.

## 2. Optimize for the system, not for yourself
The biggest mistake I feel people are making day in, day out, working in teams (or Systems) is making decisions based on personal interest and missing learning curve. This can be the Developer using a new database-backend for more performance instead of optimizing his source code for speed since he doesn't like to learn new languages, or the Manager refusing healthy optimizations to a development workflow since he isn't familiar with the new concept and doesn't want to admit.

Don't be this guy. If someone comes up with something better than you and it's worth the effort, roll with it for the good of the whole. As a DevOps, learn to think this way.

Remember, everything is a system. If `you` were the System, would you want anybody to make decisions that favor only themselves instead of the whole system? Would you want your Boss to move your position (and you) to another country just because he wants your office? This might sound non-related, but it isn't. On a daily basis, we're going to work, making decisions that only help us, but not the System that employs us.

Let's say you're a CTO insisting on writing a distributed backend in Perl on baremetal because you're scared of fancy Containers and modern Development Workflows but argument that refactoring is too dangerous for the company. Let's say most of your employees leave because they want to do something meaninful instead of constantly applying fixes to a broken System. Let's say that leaves you with a competetive disadvantage since you can't sustainably fix the system anymore, nor refactor to stay competetive because you're missing competence. I'd say you messed with the system.

Let's say you're a Junior Developer being annoyed by the grunt work Management dumps you with. You feel underestimated, underutilized and slowed down in your professional progression. You feel bored and distribute your workload broad enough to seem busy while actually having lots of time to waste on Facebook, 9GAG and Mobile Games. You either keep a low profile to get the seniority or constantly brag about how bad everything is organized while delivering unfinished work, heavily relying on those teammates that did not yet give up. While you are eager to learn, you are unwilling to do it as you don't feel motivated. Yet you don't want to speak up. I'd say, you messed with the system, too.

Finally, let's say you're the guy knowing everything about anything where you work. Let's say you're the one brought in to every major decision since you seem to have a broader picture and can be trusted. You seem to care. You're probably also one of the two other guys. You have great opportunity to either optimize or mess with the system. The way you perceive yourself and the System you're in makes all the difference.

Optimizing for a system is always dependent on its purpose. Does it serve your purpose, it's easy for you to optimize for the whole. If you feel you don't share a common purpose, you will always tend to fall into the trap of optimizing only for you which brings you out of sync with the System you're in.

From the perspective of the 3 guys, if your company solves a problem you can identify with, it's sometimes worth to step up and be more of a manager and less of a maker. There's no change without action and sometimes everybody's just waiting for `you` to take it. If unsatisfaction is your biggest problem, go talk to someone about it and get feedback. If ego is your problem, ask yourself one thing: `could you do it all alone?`

A DevOps Engineer of course is also probably one of these three guys. But while Devs develop and Ops operate, the DevOps Engineer builds bridges and pipelines and infrastructure for problems to be solved. If he stops solving the System's problems and only solves his own, he defeats his whole purpose and becomes the bottleneck. So don't optimize for yourself, kids.

## 3. Iterate, don't leap
DevOps is about doing things continuously. Integration, Delivery, Deployment, Optimization, Monitoring, Feedback, everything. This applies to Releases in modern Software Development as well as to your personal learning curve. You iterate, document, learn from it and optimize accordingly. This is a steady process and I think the one most underestimated aspect of this role within our industry. Your main job is not using specific tools for specific tasks. Your main job is to think about how to automate this process so you can solve another problem that imposes limitations on your system. To be a good thinker and problem-solver, you need to know a lot of problems and apply lots of solutions to get the right toolset. This makes the biggest part of being a good DevOps: **knowing how to solve problems efficiently**. Not how to deploy a Kubernetes Cluster from scratch (which is certainly a valuable skill). 

Unfortunately this also means to learn things outside of your core competencies. Be it `Go` as a Database-Guru or `Docker` as a Python-Dev, you need to learn about the things your system is composed of enough to understand their value and how they work. Then you can optimize for the system on your end. This also often means proposing changes to systems you don't own, for the good of the whole, which sometimes crosses social borders. `2` applies. 

Iteration, taking small steps, helps spotting problems and wrong decisions early over time, which naturally leads to a lower failure-rate. The better you know your system, the better you two will get along. 

Thinking in big release schedules requires you to manage many moving parts at once. This applies to making Operating System or Framework upgrades as well as to when you should start learning Kubernetes - read an article today instead of taking a course in April. Like anything, systems grow and develop over time. We often want to get ahead of this by introducing huge changes (into our infrastructures as well as our lives) that lead to huge emotions - either the good or the bad ones. Yet, life and IT systems share a common trait: good things take time. And how good things are within your system is something you should measure, so you know when you're falling short.

## Do I need to learn how to Code?
Absolutely yes. Today, `Everything is Code` and this is good for you. Be it a `Dockerfile` for your App, `Terraform`-Files for the Virtual Machine Clusters on AWS or `Helm Charts` for the Services on Kubernetes. Manual action on a server can and should mostly be omitted. Everything has an API today, so make use of it.

Having everything in code also relieves you from some basic documentation chores. It's easy to compile a static documentation website for your Service, App or System from `godocs` or `Swagger` or alike in a Pipeline today with automated Changelogs and Versioning by `SemVer`. Make use of these tools, get familiar with inline documentation and outline specifications in `/docs/`. Version all your Code, even if it's your Website or Notebook. Make it a habit - it helps on the long haul.

Code enables you to specifiy the state of a System as much as possible in a versionable fashion. The less you need to click in a UI, edit a configuration file by hand or care for the underlying infrastructure, the better your system is actually described and defined. This can go into a CVS like GitHub and be tested, integrated and deployed automatically by Pipelines. In the dream world of tomorrow, this means working towards `immutable infrastructure` (which still is a long way to go). 

As a DevOps, you will use a variety of "languages" over time. You will most likely not master all of them, but you will be able to use them which helps you to better integrate with existing systems. As a bonus, since you're now also a Developer, you have just learned a million new ways to automate stuff around your work and life.

## You're a manager, too
Since you're all about automating, optimizing and delivering solutions, you also need to have a good idea about the what, when and how. This requires you not only to make good decisions on these three, but also focus on the decision and its execution.

Simply put: don't go overboard.

Do what you set out to do, measure your success, iterate on it. Be your own Scrum Master and Product Owner. Accept that sometimes the thing you **need** to do isn't the thing you **want** to do. If your purpose as a DevOps is to serve the system (your personal professional carreer is also a system and you're working on it constantly), you sometimes need to be the Manager and the Maker at the same time and just do what needs to be done. This applies to the nasty Firewall-Upgrade you avoided the past three months as well as to the question if you really manage to complete the LPIC Certification you signed up for. You cannot fail even if you bust. You learned how not to do it and adjust your next attempt accordingly until the problem is solved.

Managing the emotions related to this kind of mindset is the hard part of being a good DevOps. To me, delivering a good product in a team requires management skills on all ends. If you only manage your own stuff, like most people do as most work environments are organized that way, you will always only optimize your own end. And if you fail to manage your own priorities, you will also be a bottleneck for the team - especially if you're a Solo-Guy and the team consists only of `you`.