---
layout: post
title: "My next engineering classroom is my house"
date: 2026-10-02 09:00:00 -0400
categories: [engineering, homelab]
description: "A UniFi upgrade, my first Proxmox server, and a fresh start with Codex. I'm building a home lab to turn curiosity into better engineering habits."
---

The next lesson in becoming a better engineer might start with a light switch, a movie that won't play, or a photo I need to restore.

I'm updating my home network to UniFi, turning my new AtomMan G7 Pro into my first Proxmox server, and planning a few self-hosted services: Home Assistant, Jellyfin, and Immich. At the same time, I'm setting up a new M5 MacBook Air and starting out with Codex.

That's a lot of new things at once. The thread connecting them is simple: I want to understand more of the systems I use, take responsibility for how they run, and learn from the experience. This is the starting line. I'll share the decisions, mistakes, and discoveries as the lab takes shape.

## A network I can understand

The move to UniFi is my chance to get more deliberate about the foundation. I want to understand where traffic goes, how devices find each other, and what happens when something stops connecting.

I'll explore separating everyday devices, smart home devices, and lab workloads, then work out which connections actually need to cross those boundaries. That should give me some useful questions to answer: how do I keep discovery working? How do I tell a DNS problem from a firewall problem? Can I explain a change before I make it?

Those are engineering questions. A service can be healthy on its own and still be unreachable to the person who needs it. I want more practice following that whole path.

## My first Proxmox server

The AtomMan G7 Pro will be my first server running [Proxmox VE](https://proxmox.com/en/products/proxmox-virtual-environment/features), which gives me a place to learn about virtual machines and containers on hardware I manage myself.

My initial service list is small enough to be approachable and useful enough to keep me invested:

- **[Home Assistant](https://www.home-assistant.io/):** a place to bring smart home devices together and learn to build useful automations.
- **[Jellyfin](https://jellyfin.org/):** a media server that should teach me about storage, streaming, and the path from a file on disk to playback on a screen.
- **[Immich](https://immich.app/):** a home for photos and videos, and a reason to take backup and recovery seriously from the beginning.

I expect the learning to extend well beyond getting an installer to finish. Where should each service live? What resources does it need? What gets backed up? Can I restore it somewhere clean? How will I know it has stopped working?

A photo library makes that last set of questions feel very real. One of my early milestones will be a documented restore exercise, before I rely on the lab for anything important.

## Giving the GPU some homework

I also want to experiment with the G7 Pro's GPU and learn how it might support home automation. I'm curious about local inference and whether a small model could help interpret an event or make an interaction with the house more useful.

I'll start with a bounded experiment: choose one task, establish a baseline, then measure whether adding a model helps. I'll need to learn what GPU access looks like under Proxmox, which drivers and runtimes work, and what the tradeoffs are in latency, power, and reliability. I haven't proven that setup yet; figuring it out is part of the project.

[Jellyfin's hardware acceleration documentation](https://jellyfin.org/docs/general/post-install/transcoding/hardware-acceleration/) offers another practical direction for learning about GPU workloads. I'll explore that separately as I decide how to allocate the hardware.

For home automation, the test I care about is whether the result is predictable and useful. I'll keep experiments away from essential routines until I understand how they fail.

## A fresh laptop and a new collaborator

Setting up the M5 MacBook Air gives me a chance to document my development environment as I build it: tools, configuration, and the steps I'll otherwise forget when I need to start over.

I'm also beginning to use Codex. I want to try it for scripts, configuration reviews, debugging, and documenting what I learn. My habit will be to ask for an explanation, read the proposed change, and verify the behavior myself. If it helps me move faster, I want to use some of that time to investigate more deeply.

This site is part of that experiment too: a place to turn the work into notes I can revisit and share.

## What I hope to bring back to work

As a Senior Staff QA Software Engineer, I spend a lot of time thinking about confidence in software. Running a home lab will give me more practice earning that confidence across the full system.

I'll be making small changes, defining what success looks like, checking logs, testing recovery, and writing down enough to reproduce the setup. I'll also get to live with the consequences of my decisions. An automation that annoys everyone at home is useful feedback, even if every component reports that it's healthy.

That's the hook for me: build something people actually use, then pay attention to what it teaches you. I hope to come away with stronger debugging instincts, better questions about reliability, and more empathy for the people who operate the software we ship.

First milestone: a network I can explain, one service I can restore, and notes clear enough for future me to follow. Then I'll build from there.
