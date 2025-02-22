---
title: 2023-08-30 Community Meeting
authors: [brooks]
tags: [community, meeting]
description: Agenda, notes, and recording for the 2023-08-30 community meeting
---

import ReactPlayer from 'react-player/youtube';

### Agenda

- DEMO: Rust host, OTP feature parity
- DISCUSSION: Rust host initial release, v0.78.0 (R = 18, U = 21, S = 19, T = 20; 18 + 21 + 19 + 20 = 78)
- DISCUSSION: Roadmap look
- REMINDER: [BACon](https://www.eventbrite.com/e/bytecode-alliance-componentize-the-world-tickets-681895717447) + WasmCon next week!

<!--truncate-->

### Meeting Notes

- **New Community Member!**
  - Intro to Yordis Prieto, joining us from Cuba who has been programming for a decade. He has 7 years experience working in Eilxir and React and has a background in fintech -- event-sourcing architecture. He has reached the limit of what he can do in other developer experiences and is now experimenting with wasmCloud. Welcome, Yordis! 🎉
- **DEMO: Rust Host OTP Feature Parity**
  - You can see an update in the wasmCloud/wasmCloud repo
  - We have made huge progress along the journey to WITification with a couple of small issues to resolve.
  - The good news is OTP feature parity is almost complete, with the final PR on policy-checking merging shortly.
  - Shout out to Roman, Victor and Connor for getting the Rust OTP host in shape. Amazing work.
  - What does this mean to wasmCloud devs?
    - All this hard work brings backwards compatible experience to wasmCloud when we switch to the Rust host with wash you won't notice any difference when you launch your apps.
    - When you come to launch the Rust host and run wash up, you'll see the options are the same as you would find in the wasmCloud host.
  - We can also leverage the power of Wadm manifests.
  - Crucially, this will allow us to stay close to Wasm standards as they evolve.
  - It also means we can iterate on new functionality quickly, which is the exciting part.
- **DISCUSSION: Rust Host initial release**
  - We are now running components - able to use WASI HTTP which is super exciting.
  - When will you be able to use it? We would like to release something that signifies we are making a sig release but it won't yet be 1.0.
  - We will release **wasmCloud v0.78.0** - this will be the first release of the Rust host.
  - Rapidly approaching a 1.0 release of wasmCloud, looking primarily at the stability of our SDKs and tooling rather than fundamentals of wasmCloud concepts.
- **Roadmap Review**
  - A greatway for you to see where projects are and what's coming up.
  - Roadmap: [https://github.com/orgs/wasmCloud/projects/7/views/1](https://github.com/orgs/wasmCloud/projects/7/views/1)
  - We are currently working on standardized WASI Worlds - blobstore, http, keyvalue to name a couple.
  - Defining interfaces with WIT - we are a good way along here. Our biggest challenge is wasi-cloud interfaces. There is a lot of work going on upstream in the wasmCloud repos.
- **WasmCon and BACon**
  - The schedule is packed for both events and we're super excited to see everyone.
  - Check out the schedule on the WasmCon site and take 30% off tickets with code WasmSponsor30
  - Register for our WebAssembly Workshop at WasmCon 'From Napkin Sketch to Running Your Apps at Scale'
  - Register for the Bytecode Alliance 'Componentize the World' hackathon
  - We're checking on live-streaming details and will update you in Slack.
  - Discussion on docs - agree to review docs per discussions from Justin and Yordis. Thank you for the comments and suggestions.
- **Impromptu WASI tinygo demo**
  - Check out the recording to see Jordan demo [kvcounter-wasi-go](https://github.com/jordan-rash/kvcounter-wasi-go), a wasmCloud TinyGo actor that uses _only_ wasi-keyvalue and wasi-http to run the kvcounter demo, no wasmCloud SDKs. This is the culmination of a _ton_ of hard work by Victor and Jordan to get this actor componentized.

### Recording

Check out the recording for the full discussion.

<ReactPlayer url='https://www.youtube.com/watch?v=kesWWnyFwHo' controls />
