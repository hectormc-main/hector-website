---
layout: page
title: Computer Systems Engineering
description: >
    "[S]tudents are able to design their own distributed systems to solve real-world problems. The ability to design one's own distributed system includes an ability to justify one's design choices and assess the impact of their systems on different stakeholders. "
hide_description: false
sitemap: false
---

0. unordered list to be replaced by Hydejack Table Of Contents
{:toc}

## Overview

There is *zero* programming in this class.
We study and discuss large-scale systems and their approaches.
I would describe it as a class of case-studies.

The class is not devoid of technical material however.
We covered:
* Networks - Internet, Ethernet, DNS(SEC), BGP, (DC)TCP, CDNs, etc.
* Operating Systems - Transactions, Virtualization, UNIX, etc.
* Data distribution - MapReduce, GFS, ZFS, Raft, etc.

Full scope of all technologies covered can be found [here](http://web.mit.edu/6.033/www/index.shtml).

A month into the class, the details regarding the final project is released.
This year, we are to manage the entire electrical grid of a city.
The city has batteries and solar panels. Try to limit amount of electricity we buy from neighboring city.

There are limited resources we have to work with and our city must be disaster-resistant.
Our goal was to design, justify, modify, and defend our design in our final paper.

## Stakeholders

Before we discuss cases, we must first consider who it impacts.
This is something MIT has been trying to push for the last couple of years.
Thinking beyond implementation but *impact* has been eye-opening to me.
Early designers were not too concerned about the impact of their work, more just making it work.


## Case Studies

There are far too many cases to cover here.
Instead, I will cover those I found particularly interesting.

### [Meltdown](https://meltdownattack.com/meltdown.pdf)
Click the title for the paper if you would like to read more.
{:.note}

The infamous Intel exploit that took advantage of cache optimization.
An interesting case to think about because - at first glance - it appears unavoidable without completely removing out-of-order execution.
Out-of-order execution is one of the fundamental CPU accelerations and its emergency patch severely impacted performance of many older computers.

### [GFS](http://web.mit.edu/6.033/www/papers/gfs-sosp2003.pdf)

I appreciate this paper not because of its content but because of the seeds of thought it has sown into me.
I can't but think about storage anymore without thinking about how its distributed authority and accesses work.

### [DNS](http://web.mit.edu/6.033/www/recitations/02-dns.shtml)

It's a name to IP mapping.
Not super interesting but it did kick-off me understanding just *what is* the *internet*.


## Final Project

### [Set-up](http://web.mit.edu/6.033/www/assignments/dp.pdf)

There's a lot to the set-up, but to keep it brief, there are three pieces of hardware:
* Smart meter - Connected to each house and keeps logs of electricity. Is **not** programmable with additional functionalities. Has limited storage and small battery.
* Microgrid controllers - Controls 10 smart meters. Is programmable. Limited storage and computation.
* Central utility - Headquarters. Big battery and very limited bandwidth. Has solar panel farm.

When a house is out of battery, it may either get power from houses in its microgrid or from the Central Utility.
This is our main method of interaction with
Should the situation become dire, we may also cut off microgrids from the Central Utility should we want to power a hospital for instance.

Power is cheaper to buy from neighboring cities when it is nighttime.

We have to manage:
* House/Central Utility Battery level
* Microgrid Prioritization
* Microgrid/Central Utility Bandwidth
* Everyone's storage

### Design Decisions

The general gist of our decisions were around adaptability.
We wanted a system that evolved over time and approached a relative ideal compared to a static system.

We knew not to use a traditional Machine Learning model for that is an ill-fit to our system.
Instead, it's *reinforcement-learning-inspired*.
Meaning that, when the day is done, the parameters of the system are given a score.
Based on performance, the parameters shift a bit to try to find a better setting.
Parameters may only shift within a certain range to stop catastrophes.

There are several models that the system switches between depending on external conditions such as weather and time.

To be sensitive to limited bandwidth, we created *regions* of 10 microgrid controllers with a rotating *lead*.
A region of microgrid controllers all share equal settings.
Regions reduce bandwidth and computation load on the Central Utility.

For our full report see:

## Our CHEESE System Report

{% pdf "Design_Project_Report___Hector__Helen__Michael.pdf" %}
