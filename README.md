# Jalen Edusei

**Computer Systems Engineer.** B.S., University of Georgia, Morehead Honors College, May 2026, cum laude.

[jalenedusei.com](https://www.jalenedusei.com) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/jalenedusei/) &nbsp;·&nbsp; [CV](https://www.jalenedusei.com/cv.pdf) &nbsp;·&nbsp; jalen.edusei@gmail.com

I work from bare metal up: ESP32 and FPGA firmware, macOS systems programming in Swift, and full-stack web. I am looking for full-time new-grad roles in software, embedded, or full-stack engineering.

The habit that runs through everything below is measuring instead of asserting. Each project ships with the number that justifies it, and when the answer was no, the repo says so.

---

## Selected work

### Systems and AI infrastructure

| Project | What it is | The measurement |
| --- | --- | --- |
| [Exocortex](https://github.com/jke48222/exocortex) | Local-first memory every AI tool can share, over one frozen MCP contract | 100,106-event encrypted store; recovered 31,328 iMessages out of Apple's typedstream `attributedBody`; hybrid BM25 and binary-vector retrieval finds the right document 95% of the time on paraphrased queries against 55% for keywords alone |
| [WindowPet](https://github.com/jke48222/WindowPet) | A desktop creature that treats your real macOS windows as platformer terrain | 12,500 lines of zero-dependency Swift, 131 tests, ballistic leaps landing within 1.5 points, 0.24% CPU asleep in 48 MB |
| [Screen-Coach](https://github.com/jke48222/screen-coach) | Name any on-screen control and a cursor lands on it, accessibility tree first, local vision model only as fallback | A warm ScreenCaptureKit stream beat the `screencapture` CLI 7.9 ms to 204 ms at p90; batching cut per-node attribute reads 3.1x; 12 of 12 targets on Chrome |

### Backend and data

| Project | What it is | The measurement |
| --- | --- | --- |
| [Relay OMS](https://github.com/jke48222/relay-oms) | Event-driven order management on Elixir and Phoenix that refuses to oversell | Row-locked allocation across four fulfillment centers behind a database constraint that makes oversell unrepresentable; `Idempotency-Key` replay returns the original order; an 8-state machine where a lost race resolves to a clean 409 |
| [Live Election Platform](https://github.com/jke48222/live-election-platform) | Presenter-paced live voting; a campus election ran on it with real candidates | 14 races and 39 candidates on a dues-checked roster, one vote per position enforced by a database constraint rather than the interface, so a duplicate gives an attacker no signal. Multi-tenant rewrite on plain Postgres with row-level security that fails closed |
| [Trading harness](https://github.com/jke48222/trading-harness) | Paper-account backtesting run like research, not like a demo | 7 pre-registered trials in an append-only ledger, 114 runs across 52 configurations, in-sample and out-of-sample splits, 10,000-resample bootstrap under Bonferroni. One portfolio-level effect survived, at t = 2.91 |

### Embedded and hardware

| Project | What it is | The measurement |
| --- | --- | --- |
| **AnimalDot** (capstone) | A pet bed that measures heart and respiration rate without touching the animal | A geophone under the mattress picks up the mechanical shock of each heartbeat; DC removal, kurtosis-based motion rejection, and a hand-rolled forward-and-backward Butterworth pass on the microcontroller for zero phase distortion. Respiration is recovered by amplitude-demodulating the heartbeat envelope |
| **PrimeForge** (FPGA) | Segmented Sieve of Eratosthenes and trial-division engine on a Nexys A7-100T | Direct indexing inferred thousands of tiny RAM primitives, so every access was restructured into a three-phase registered read-modify-write that maps onto block RAM. On the board it counted all 5,761,455 primes below 100 million |
| [PARMCO](https://github.com/jke48222/parmco) | An iPhone that spins a real 12 V motor over BLE, with no Bluetooth framework in between | A 2,337-line GATT server written by hand on BlueZ and GDBus, a NoInputNoOutput pairing agent so the phone reconnects unattended, 20 kHz hardware PWM, and RPM telemetry streamed back every 200 ms |
| [Album-Art LED Matrix](https://github.com/jke48222/album-art-matrix) | An LED wall that shows whatever is playing, over a colour-managed HUB75 pipeline | A C render daemon pinned to an isolated CPU core so no scheduler hiccup shows as a bright row; the backplane program emits its own netlist and BOM, 76 parts across 105 nets, sized in ngspice: 33 ohm series termination cut overshoot from 8.71 V to 6.48, and an NTC limiter cut inrush from 275 A to 15.8 |
| **MEMESat-1** | Flight software for UGA's CubeSat mission on NASA's F Prime, deployed to a Raspberry Pi CM4 | 90% line coverage, 60% branch coverage |
| [Audio Tracking Car](https://github.com/jke48222/Audio-Tracking-Car) | A Raspberry Pi car that localizes and drives toward a sound source | Dual-microphone analog front end, ADC signal processing, and PID motor control with optical encoder feedback |

### Web, graphics, and XR

| Project | What it is | The measurement |
| --- | --- | --- |
| [Edusei Workstation](https://github.com/jke48222/Edusei-Workstation) | My portfolio, rebuilt as VS Code in the browser so every project is a file you can open | 16,000 lines of TypeScript covering explorer, quick open, command palette, full-text search, a typeable terminal, and nine themes. The landing page scrubs video frame by frame against scroll with no animation library; keeping three.js out of the eager bundle cut 310 KB gzipped from first load |
| [KUL Enterprises](https://github.com/jke48222/kul-enterprises-website) | Production site for a Georgia freight carrier, shipped solo and live at [kulenterprises.com](https://kulenterprises.com) | 12 style directions built as 20 variants before landing 22 static pages on an 88-property token system; every word editable in a git-backed CMS across 19 typed collections; 482 lines of my own search scoring prefix, one-edit-typo, and run-together matches against a 36-term freight synonym sheet; WCAG AA with ink measured at 12.25 to 1 |
| [Akilah Mali](https://github.com/jke48222/akilahmali) | Official site for an independent Atlanta artist, live at [akilahmali.com](https://www.akilahmali.com) | Music and tour dates arrive through live services rather than hardcoded lists, so nothing on the page can go stale between releases. Static Next.js 16 and React 19 with one API route and no backend to keep running |
| [Ashfall](https://github.com/jke48222/ashfall) | A time-travel puzzle framework in Unreal: one Pompeii block toggles between the living city and the eruption | The authoritative state machine lives in an editor-world subsystem, so 32 assertions drive the entire loop headlessly with no window and no person. 1,333 lines of C++ over a procedurally built level. Never played, and the README says so |
| [Kitchen Chaos VR](https://github.com/jke48222/VR-Final-Project) | Two-player Overcooked in VR for Quest 3, where you physically catch what you drop | 120-second rounds across 29 randomized themes; movement written against the raw input system rather than a locomotion rig, including a projectile-simulated teleport arc; a language model performs the verdict on each plate |
| [VR Portfolio 1](https://github.com/jke48222/VR-Portfolio-1) and [2](https://github.com/jke48222/VR-Portfolio-2) | Unity XR demos for Quest 3: transformation, physics, and interaction, then a VR museum and a mixed-reality room | Spatial audio, depth occlusion, passthrough, hand tracking, and an NPC assistant on Wit.ai with lip-synced responses |
| [Übersicht widget suite](https://github.com/jke48222/widget-suite) | 12 desktop widgets for macOS, each its own repo | Now playing as a spinning record, a dot-matrix travel globe, clipboard history with secret masking, NASA APOD, and nine more |

Some work is not linkable here because the repositories are private: a broker-vetting and credit-limit portal for a freight carrier where every judgement is permanent and attributable, and a damage-claim evidence verifier that treats the photo as evidence and the accompanying text as a suspect, with a twelve-pattern prompt-injection detector that force-flags a row so it can never auto-resolve.

---

## Stack

**Languages** &nbsp; C, C++, Swift, Python, TypeScript, JavaScript, C#, Java, Verilog, ARM assembly, SQL, MATLAB, R

**Embedded and hardware** &nbsp; ESP32, STM32, Raspberry Pi, PlatformIO, Zephyr RTOS, NASA F Prime, MQTT, NimBLE, BlueZ, Vivado, Nexys A7, PCB design, ngspice, signal processing

**Web and backend** &nbsp; React, Next.js, Node.js, Elixir and Phoenix, PostgreSQL, Supabase, Tailwind, Vite, Three.js and React Three Fiber, Docker, Vercel

**Apple and XR** &nbsp; SwiftUI, AppKit, Core Text, ScreenCaptureKit, Accessibility APIs, Unity, Unreal, OpenXR, Meta XR SDK

**AI** &nbsp; Model Context Protocol, agentic tool-use loops, local quantized vision and embedding models, retrieval systems

---

## Background

University of Georgia, B.S. Computer Systems Engineering, Morehead Honors College, May 2026, cum laude. Tau Beta Pi. Vice President of NSBE at UGA. Brother of Theta Tau. Former Capital One intern.

Outside the terminal: songwriting, half marathons, and a standing argument that the album cover belongs on a wall rather than a lock screen.
