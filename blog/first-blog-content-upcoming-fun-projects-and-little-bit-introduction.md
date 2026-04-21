---
title: "First Blog Content : Upcoming Fun Projects and Little Bit Introduction."
date: "April 21, 2026"
description: "Welcome to my first blog post! I'm Faiz, and I'll be using this space to share my tech experiments and learning journey. In this debut post, I dive into three projects currently in the works: Ledengsploit, an experimental pipeline workflow for pentest automation; an agent-based Intrusion Detection System with detailed forensic fingerprinting for my university assignment; and a hybrid hydroponics system that I'm prepping for future IoT automation."
image: ""
tags: [""]
featured: false
published: true
---

Hello guys, my name is Faiz Nurdiana, you can call me Faiz. That’s it, I won’t tell anything further hehe.

So, this is my first post in the blog section. We’ll be talking about things I like, mostly technology-related stuff or knowledge I’ve picked up along the way (because I really enjoy learning new things). But it might also include some non-IT topics too (because hey, knowledge is knowledge, right? :p).

So yeah, that’s it for my introduction. I’ll be revealing some projects that are currently in the making. These projects are in different fields, but still within the IT corridor (one of them only touches it a little bit, while the others are heavily IT-related). The projects are :

---

## 1. Ledengsploit (Very Experimental)

**Github:** [https://github.com/0xfzz/ledengsploit](https://github.com/0xfzz/ledengsploit)

The name is a little bit weird, right? If you’ve done pentesting before, you know how it feels to create new automation checks and manually chain them into other tools, that must frustrate you a lot, right? Or maybe not? If you’re not feeling it, I definitely felt it (sad).

So, what does this new project do to make things easier, *bang* (bro)?

Okay, good question (I asked it myself). This project is basically a pipeline-based workflow for pentest automation. Sounds a bit familiar, right? Yes, I took inspiration from n8n. Even though I’ve never actually used it before, I think it follows the same concept (I’ll probably use it eventually; maybe it will boost my workflow).

### How it works

That's it for the explanation. I’ll explain the detailed technologies that I used to make the project later in the Project Section, if the project is usable.

- A pentester can create new automation tools using this project's plugin base module. This module allows you to integrate the tools you build directly into the project ecosystem.
- Next, the pentester can create a new workflow from the "Workflow Creation" section. You can name the workflow and add a description, just to prevent you from forgetting the purpose of the workflow you made.
- After that, you arrange the pipeline. The pipeline itself consists of 3 main phases and 1 Input pipeline. You can arrange multiple tools within the pipelines themselves (except for the Input pipeline). These pipelines are :

### The Pipelines

- **Input Pipeline**
  This pipeline is for reading the target list (e.g., IPs, domains, or anything else). It can handle raw text and file inputs.
- **Pre-process Pipeline**
  This is for processing the input before you pass it to the Standard Pipeline. Examples include parsing the input, formatting it, or anything else needed to prepare the data.
- **Standard Pipeline**
  This is the main part of the pentesting cycle, you can add multiple pipelines in this Standard Pipeline and you can name it the phase that you want (e.g., Recon Phase, Scanning Phase, and Exploit Phase).
- **Post-process Pipeline**
  This is where you can process the data flow from the Standard Pipeline, this Post Process is basically for report generation, severity calculation based on the exploit, or you can output which target that successfully exploited.

---

## 2. PUI (Proyek Utama Informatika) - Injection Detection System

**Project Type:** Injection Detection System based on Regex (Maybe Private Project)

Okay, before we get into the project, I’ll explain what PUI is. PUI, or Proyek Utama Informatika, is a project-based assignment from my university. Basically, we as students should make anything as long as it's related to our major, Informatics. I chose to focus on RPL (Rekayasa Perangkat Lunak or Software Engineering), so that is what I decided on to finish this assignment.

What does this project do? It is just like an IDS in general, but with more detailed forensic information. I used a lot of data, for example, OWASP Injection ([https://owasp.org/Top10/2025/A05\_2025-Injection/](https://owasp.org/Top10/2025/A05_2025-Injection/)) and the OWASP CRS Ruleset ([https://github.com/coreruleset/coreruleset](https://github.com/coreruleset/coreruleset)), to make this project possible.

### Project Features

- It can be installed on one server and can listen to many servers' logs because I made it agent-based, using Fluent Bit to stream the data.
- It can generate an Executive Summary for 30 days of threat information.
- It records fingerprints using JA4H ([https://github.com/FoxIO-LLC/ja4/blob/main/technical\_details/JA4H.md](https://github.com/FoxIO-LLC/ja4/blob/main/technical_details/JA4H.md)).
- So, any threat can be grouped into a single fingerprint, and it records the IP addresses that have a tie or connection with that fingerprint.
- Notification alerts for highly critical threats. The notification system is also pluggable, anyone using this project can add a new plugin to listen for alerts (e.g., a Telegram plugin, or anything like that).

---

## 3. Hydroponic System

**Status:** Manual setup (Transitioning to IoT)

This sounds like I might be out of my expertise, right? Yesn’t. I created a hydroponic system because I want to implement it with IoT devices to automate anything measurable in hydroponics. But for now, it's still manual (budget-related issues).

Here is what I’ve created so far:

A water gutter-based hydroponic setup that has two holes, top and bottom, at the front of the gutter. What does it do? Why not just put one hole? That is because I want to implement two different hydroponic systems (NFT and DFT). FYI:

- NFT, or Nutrient Film Technique, is a hydroponic system that relies on flowing water continuously. Water from the source → Hydroponic NFT System → Back to the source. This system has a con: when there is an electricity outage, the water in the pipe or gutter will run out, and the plants won't get the water or nutrients they need.
- DFT, or Deep Flow Technique, is a hydroponic system that, just like NFT, flows water, but it leaves some water in the pipe or gutter because the drainage hole is not all the way at the bottom. So, when there is a power outage, it's safe because the plants have reserve water in the pipe.

### Next Plan: Automation

My next plan is to make the system more monitored and automated. The systems I want to automate are fault tolerance (switching to DFT when there is a power outage), nutrient-filling automation when the PPM meter shows that the water is low on nutrients, and water-filling automation when the water level is not within the variables I define.

---

That’s all for this first blog post. If you have any further questions you can email me on [faiz@0xfzz.my.id](mailto:faiz@0xfzz.my.id). I’ll see you in the next one!