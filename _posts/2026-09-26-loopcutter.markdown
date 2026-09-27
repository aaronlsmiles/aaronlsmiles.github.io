---
layout: post
title: "loopcutter: sample-accurate loops for live sets"
course: open-source tool
date: 2026-09-26 12:00:00 +00:00
image: /images/loopcutter.png
categories: projects
code: https://github.com/aaronlsmiles/loopcutter
---
An open-source Python tool that cuts loops out of full tracks for live, loop-based DJ sets, where dozens of short loops from different records play at once. It finds each track's beat grid, reads loops marked by ear in rekordbox or Serato, and snaps each start onto the beat, reporting every move. Every loop's length comes from its tempo and bar count, rounded once, so loops can run together for minutes without drifting apart. It builds roll variations for clip launchers, separates stems, tags and files the loops for a sample browser, verifies every file with checks that can fail, and works out which session keys a library can be pitched into.
