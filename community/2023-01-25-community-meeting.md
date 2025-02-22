---
title: 2023-01-25 Community Meeting
authors: [brooks]
tags: [community, meeting]
description: Agenda, notes, and recording for the 2023-01-25 community meeting
---

import ReactPlayer from 'react-player/youtube';

### Agenda

- DEMO: Distributed wasmCloud on GCP, Local, and a Raspberry Pi!
- wasmCloud Roadmap: Now, next, and ideas
- Follow-up discussion on actor nomenclature

<!--truncate-->

### Meeting Notes

- Demo
  - Brooks showed the key-value counter application running across 3 wasmCloud hosts, one in GCP, one on a local macbook, and one on a raspberry pi
  - Follow up discussions included details about lattice invocation round-robining, how wadm does reconciliation, and rollout strategies
    - Information about the lattice can be found [here](https://wasmcloud.com/docs/reference/lattice/), around how the network can handle new wasmCloud hosts, terminated wasmCloud hosts, and round-robin requests between available compute
    - Information about wadm can be found with [the source code](https://github.com/wasmcloud/wadm). Participants in the call spoke about the reconciliation loop and how wadm will automatically adjust where application components run based on a declarative spec based on the [Open Application Model](https://oam.dev/)
- wasmCloud Roadmap
  - Please leave comments on our PR! https://github.com/wasmCloud/wasmCloud/pull/269
  - The wasmCloud roadmap is divided into three categories: Now, Next, and Ideas
    - Now contains work that is planned and prioritized for the short-term
    - Next contains work that is planned, but not prioritized for the short-term
    - Ideas contains experimentations, possible future work, and serves as a good place for a "have you thought of this" section in our roadmap
    - Any community members or open source contributors are more than welcome to take issues pertaining to the roadmap, and we plan to mark beginner issues with a `good-first-issue` label to deliniate great starter issues
- Actor discussion
  - Due to preconceived notions on the actor model, we discussed renaming our wasmCloud WebAssembly modules from Actor to something else
  - Our current [Actor Documentation](https://wasmcloud.com/docs/reference/host-runtime/actors) for reference
  - We decided in the call, community and maintainers, to keep the Actor nomenclature and focus on education around the term and properly describing our compute terminology (which the actor in an actor model accurately describes what our wasmCloud actors do)

### Recording

<ReactPlayer url='https://youtu.be/Ua07aKGWPOI' controls />
