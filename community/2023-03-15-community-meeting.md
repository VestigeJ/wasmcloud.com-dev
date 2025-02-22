---
title: 2023-03-15 Community Meeting
authors: [brooks]
tags: [community, meeting]
description: Agenda, notes, and recording for the 2023-03-15 community meeting
---

import ReactPlayer from 'react-player/youtube';

### Agenda
- DEMO: Link definitions & link names: their meaning, usage, and some powerful things you can do 
- WASI wasmCloud component model update with Roman
- Proper use of wasmCloud github projects with Taylor 
- SCALE 20x recap + recordings
- Hackathon progress / callouts

<!--truncate-->

### Meeting Notes
#### Link Definitions and Names: Brooks
We talk a lot about these and, most of the time the purpose is to link an actor to a capability provider at runtime, and provide some config for that link. We often gloss over Link Names as they are not needed in 90% of use cases. Why? Because default works - don't have to supply a link name. However there are some useful uses:

- Link Names are the logical separation - you can run diff instances of capability providers.
- For specific use cases it is really useful to have additional link names.
- Useful when you want to run everything on local to a staging env - put it from laptop to cloud.
- Link Names allow you to do this in a gradual way - great for canary testing and AB/failover.
- Another way - see demo - is to connect a KV counter with a different link name.
- Diff link name with a provider call - you have to call 'With Link' function.
- Benefit: publish to diff providers, store the same info in different databases.

#### WASI component model update - Roman
- The big news is wasmCloud now has support for Components!
- This is, essentially, the first working example of the Component Model working, and it's working in wasmCloud.
- Rust SDK allows us to load actors within wasmCloud with a high level - a different binary API.
- We have switched to the latest and greatest from wasmtime and WASI Preview 2.
- You can compile your Wasm and call whatever function you want in that Wasm actor.
- Local developer docs are now available (link)
- Next: Polishing the API

#### GitHub Projects - Taylor
- Review of how it could work and how we would like to see it used by both maintainers and contributors.
- Taylor demoed how all current requests are triaged [link] which is making it easier to prioritise and see everything in one place.
- Issues management should be, from now on, much easier to view and manage.
- Click here for access.

#### Wasm I/O talks
- Bailey will demo, for the first time, the Component Model in action in wasmCloud at wasm I/O in Barcelona next week.
- Taylor and Bailey will also get together to give a wasmCloud workshop - details below - if you're in Barcelona, don't forget to look us up.
- 23rd March @14.20 - 16.15 CET: wasmCloud Crash Course with Cosmonic - Bailey Hayes and Taylor Thomas
- 24th March @ 15.30 - 16.00 CET: WASI-Cloud: the Future Of Cloud Computing With WebAssembly - Bailey Hayes and Microsoft's Dan Chiarlone.

#### Devpost Distributed Application Hackathon Office Hours
- Good news! All those taking part (and interested) in our devpost Hackathon can join us today at 3pm EST on Discord to ask questions, work through issues, or just come hang out with Cosmonic developers. Please join us on Discord and then sign up for the event if you're interested.
- Check out our update here, can't make this session? No worries, we'll look to hold office hours each week until the end of the hackathon.

### Recording
Recording is being uploaded to YouTube and will be displayed promptly

<ReactPlayer url="https://youtu.be/1wXDKORz1pg" controls />
