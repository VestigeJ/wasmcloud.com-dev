---
title: 2023-10-04 Community Meeting
authors: [brooks]
tags: [community, meeting]
description: Agenda, notes, and recording for the 2023-10-04 community meeting
---

import ReactPlayer from 'react-player/youtube';

### Agenda

- DISCUSSION: WASI-fills newness.
- DISCUSSION: [Versions](https://docusaurus.io/versions) in wasmCloud documentation. Would like to determine what a "version" is for the wasmCloud project.
- DISCUSSION: Hacktoberfest! 🎃

<!--truncate-->

### Meeting Notes
**UPDATE: WASI-fills Newness - Taylor**

- Much is moving fast in the world of Wasifills - here’s an up-to-the minute update on what’s new.
- In the Rust ecosystem cargo components are stabilising - allowing you to select and swap different components.
- Roman had the exciting idea to dynamically generate Wasifills on the fly! 🤯
- Because Wasm modules have their interface definitions embedded, we are able to look at what an actor is importing and exporting and, therefore, dynamically generate stubs.
- MessagePack is commonly used to send messages back and forth.
- WASI plugins are the future but, right now we’re enabling you to write your components the host will dynamically generate the stubs to carry out the serialisation on the fly.
- Depending on how all this experimentation goes, we will update the Wasifill RFC with this new functionality.
- If we get this working NONE of this has to be in wash. A hopeful future - let’s see how this goes.
- Tune in next week to (hopefully) see this in action.

**DISCUSSION:** Hacktoberfest! 🎃

- 10th year of Digital Ocean’s event. [Hacktoberfest.com](http://Hacktoberfest.com) brings together open source maintainers who are eligible to designate their open source project for Hacktoberfest.
- All you need to do is to close or have 4 approved pull requests on Github or GitLab.
- One you have this, DigitalOcean will plant a tree on your behalf and send you a nice virtual badge.
- All you need to do if you want to partake is sign up on the website.
- On the wasmCloud side we’ll designate our good issues and some stretch issues with the goal to lower the barrier to people are getting started in Wasm.
- It officially starts tomorrow at 11am EDT.

**DISCUSSION: [Versions](https://docusaurus.io/versions) in wasmCloud documentation. What is a "version" is for the wasmCloud project.** 

- We use Docusaurus to manage our documentation. It has a load of different features - including the ‘version’ feature.
- If you’re using a specific version of Docusaurus, you can change the posture of the information you see. It will be really important to designate between versions of documentation.
- For example, wasmCloud is not just one entity - it’s comprised of the versions of wash, wadm etc. you’re currently using.
- Kevin’s view: the newest version of docs really is all that matters. Old stuff is deprecated. Concurrent supported releases - where they are different enough to have sep docs. Until we have something like that, this could be overkill at this stage.
- Yordis: tags - old versus new. Easy to discern.
- Takeaway: We plan to be clear when we introduce new functionality in new versions to indicate that in the documentation for a time, but we do not plan to preserve multiple versions of documentation at this time.

Don’t forget to check in on the latest [wasmCloud roadmap](https://wasmcloud.com/docs/roadmap) and join the conversation in the [wasmCloud Slack channel](https://wasmcloud.slack.com/).

### Recording

<ReactPlayer url='https://www.youtube.com/watch?v=3KUZf4Rd5dg' controls />
