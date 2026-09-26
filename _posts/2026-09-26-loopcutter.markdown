---
layout: post
title: "loopcutter: sample-accurate loops for live sets"
course: open-source tool
date: 2026-09-26 12:00:00 +00:00
image: /images/loopcutter.png
categories: projects
code: https://github.com/aaronlsmiles/loopcutter
---
An open-source Python tool that cuts loops out of full tracks for live, loop-based DJ sets, where dozens of short loops from different records play at once. Every loop's length comes from its tempo and bar count, rounded once, so loops can run together for minutes without drifting apart. It snaps each start to a zero crossing, builds roll variations for clip launchers, checks every file it writes, and works out which session keys a library can be pitched into.
