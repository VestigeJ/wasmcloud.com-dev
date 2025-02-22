---
title: 2023-07-19 Community Meeting
authors: [brooks]
tags: [community, meeting]
description: Agenda, notes, and recording for the 2023-07-19 community meeting
---

import ReactPlayer from 'react-player/youtube';

### Agenda

- DEMO + DISCUSSION: Update on wit-ified providers
- DISCUSSION: RFCs & ADRs in the wasmCloud org

<!--truncate-->

### Meeting Notes

- DEMO + DISCUSSION: Update on wit-ified providers - Jordan
  - Last week Jordan demoed wash-call -- triggering the actor and the health calls the provider carries out.
  - Soon after, he was able to debug the final msgpack error.
  - We now have, within the wasmCloud OTP host, a provider and actor that are able to communicate using wit-generated contracts - this is a really exciting development.
  - Jordan added an update in [Slack](https://wasmcloud.slack.com/archives/CS38R7N9Y/p1689614679564239?thread_ts=1689614070.861139&cid=CS38R7N9Y): sharing the ping pong example and provider sdks that were moving from Smithy to wit contracts and a small update on next steps.
  - We've created what we call wasifills -- code generation for wit, specifically for wasmCloud, which brings all the encoding/decoding/message pack logic.
  - To do that we had to be able to parse a wit file.
  - The only thing that exists is a wit parser written in Rust that is published on the Bytecode Alliance's github repo - Rust wasn't the preference here.
  - Jordan rewrote most of the wit parser in Go so it becomes a native Go library - all the tests are passing right now (adds ability to remove cgo from equation).
  - Jordan's Go-wit parser: [https://github.com/jordan-rash/go-wit](https://github.com/jordan-rash/go-wit)
  - We now have a parser that will allow Jordan to generate wasifills by next week - stay tuned for next week's meeting.
  - Once we have this, we can wrap it in wash -- `wash build` will be able to see wit files and generate witified code.
  - WIT is a standard within the W3c and WASI working group. It is part of the IDL we're using to define high level interfaces.
  - Recommend catching the recording for the deeper discussion on wasifills, the component model and more.
- DISCUSSION: RFCs & ADRs in the wasmCloud org - Brooks
  - In response to a question on wasmCloud slack that suggested we could use some more detail on the RFC/ADR process in the wasmCloud org.
  - What's the difference between RFCs and ADRS?
    - RFCs can be of any scope - anything from beginner questions to a large-scale change request.
    - ADRs are more strategic architectural decisions or major infrastructure changes - longer-term commitments.
  - RFCs
    - There have been a ton of exciting RFCs on the wasmCloud side: many from Kevin - detailing many exciting changes in the wasmCloud ecosystem - rust-based host, defining interfaces with wit for example.
    - They should not be difficult to contribute for community members.
    - It should be easy to see where we are.
    - We wrote an [RFC about RFCs](https://github.com/wasmCloud/wasmCloud/issues/381)!.
    - Aim: to provide an easy understanding for visitors as to where we are and encourage people to submit them on their own, even if you have not submitted an RFC before.
    - To make it easy for people to be able to find an accepted RFC for well-defined and scoped features. This in turn should make it easier to deploy new features.
    - We think it should not be an arduous process that focuses on issues.
    - Simple labels for RFCs will help.
  - ADRs
    - Architectural decision logs are saved [here in the wasmCloud/wasmCloud repository](https://github.com/wasmCloud/wasmCloud/tree/main/adr).
    - Some of them are baseline - using NATS jetstream, committing to distributed capabilities etc.
    - For example: where it comes to communicating across distribution network boundaries - NATS is our formal, recorded option.
  - Discussion in the call spurred an addition to the RFC, where each RFC, when completed, should be closed by submitting an ADR with the decision.

### Recording

<ReactPlayer url='https://www.youtube.com/watch?v=oy4qrYTMBFo' controls />
