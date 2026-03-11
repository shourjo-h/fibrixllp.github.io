---
title: "The Speed of Light Is Too Slow: Why Latency Is the Real Battle"
date: 2026-03-14
author: shourjo
category: Technology
tags:
  - technology
  - broadband
  - latency
  - fiberoptic
description: Your ISP promises gigabit speeds, but light through fiber only travels at 70% its vacuum speed. Why latency — not bandwidth — is the true bottleneck of the modern internet.
image: ""
---

Here's something that should bother you: **the speed of light isn't fast enough for the internet**.

That sounds absurd. Light travels at 299,792 km/s in a vacuum — fast enough to circle the Earth 7.5 times in a single second. But inside a fiber-optic cable, light doesn't travel through a vacuum. It travels through **glass**. And glass slows it down.

Light in fiber moves at roughly **200,000 km/s** — about **68% of its vacuum speed**. That 32% penalty is the refractive index of silica glass, and it's one of the reasons your online game lags, your video call stutters, and your stock trade executes 3 milliseconds too late.

## Bandwidth vs. Latency: The Pipe Analogy

ISPs love to advertise bandwidth: **100 Mbps! 500 Mbps! 1 Gbps!** But bandwidth is only half the story.

Think of it this way:

- **Bandwidth** is how wide the pipe is — how much water can flow through at once.
- **Latency** is how long it takes for the first drop of water to travel from one end to the other.

A 1 Gbps connection with 100 ms latency will feel slower for everyday use than a 100 Mbps connection with 5 ms latency. That's because most internet activities — loading webpages, gaming, video calls — are **latency-sensitive**, not bandwidth-sensitive.

### What Matters for What

| Activity | Bandwidth Sensitive? | Latency Sensitive? |
| --- | --- | --- |
| Streaming 4K video | Yes | No (buffered) |
| Video calls (Zoom, Meet) | Moderate | **Very** |
| Online gaming | Low | **Critical** |
| Stock trading | Low | **Critical** |
| Web browsing | Moderate | **High** |
| File downloads | **Very** | Low |
| Cloud gaming (GeForce NOW) | High | **Critical** |

## Where Does Latency Come From?

Latency isn't just about the speed of light in fiber. It's the sum of multiple delays:

### 1. Propagation Delay

This is the physics part — the time light takes to physically travel through the cable. Mumbai to London through submarine fiber is approximately **12,000 km**. At 200,000 km/s, that's **60 ms one way, 120 ms round trip** — and that's the absolute theoretical minimum.

### 2. Processing Delay

Every router, switch, and firewall your data passes through adds a small delay. A typical packet might pass through **15–20 network hops** between you and a server. Each hop adds **0.5–2 ms**.

### 3. Queuing Delay

When a router is congested, packets wait in a queue. During peak hours, this can add **10–50 ms** or more. This is why your internet "feels slow" at 9 PM even though a speed test shows full bandwidth.

### 4. Serialization Delay

The time it takes to push a packet's bits onto the wire. At gigabit speeds this is negligible, but on slower last-mile connections it adds up.

### 5. Last Mile Delay

The connection from your ISP's network to your home matters enormously:

| Last Mile Technology | Typical Latency Added |
| --- | --- |
| FTTH (Fiber) | 1–3 ms |
| Cable (DOCSIS 3.1) | 5–15 ms |
| DSL (Copper) | 10–40 ms |
| 4G LTE | 30–50 ms |
| 5G (mmWave) | 5–10 ms |
| Satellite (GEO) | 500–700 ms |
| Satellite (LEO/Starlink) | 25–50 ms |

This is why **fiber-to-the-home** isn't just about speed — it's about giving you the lowest possible latency at the last mile. The difference between 1 ms (fiber) and 40 ms (DSL) might seem small, but it **compounds** with every request your device makes.

## The High-Frequency Trading Arms Race

Nowhere is the latency obsession more extreme than in **financial trading**. In this world, a **1-millisecond advantage** can be worth millions of dollars per year.

Trading firms have:

- Built **private microwave relay towers** between exchanges (microwaves travel at 99.7% of light speed in air vs. 68% in fiber) — saving ~4 ms between Chicago and New York.
- Lobbied for **the straightest possible fiber routes**, because every slight bend in the cable adds microseconds.
- Used **hollow-core fiber** — experimental cables where light travels through air inside the fiber, achieving ~99% of vacuum speed.
- Co-located servers **inside the exchange building** to shave off the last microseconds.

The irony: the entire stock market has been physically redesigned around the speed of light being too slow.

## The Latency Map of India

For Indian internet users, latency depends heavily on **where the content server is**:

- **To Mumbai (domestic CDN):** 5–20 ms from most metro cities
- **To Singapore:** 50–80 ms
- **To Europe:** 100–150 ms
- **To US East Coast:** 150–200 ms
- **To US West Coast:** 200–280 ms

This is why **Content Delivery Networks (CDNs)** exist. Netflix, YouTube, and Hotstar don't serve you video from a server in California — they cache it on servers in Mumbai, Chennai, or Kolkata. The data only has to travel the last few hundred kilometers to reach you, keeping latency under 20 ms.

Every major ISP, including Fibrix, peers with CDN providers to keep this local-content latency as low as possible.

## The Race for Shorter Routes

The global push to reduce latency has led to some remarkable engineering projects:

- **Arctic submarine cables** — a cable through the Arctic from Tokyo to London would be ~30% shorter than the current route through Southeast Asia and the Suez Canal.
- **The Equiano cable** (Google) — takes a new route down the west coast of Africa, adding a shorter path between Europe and South Africa.
- **Hollow-core fiber** — still experimental, but if it scales, it could reduce in-fiber latency by **30%** instantly.

## What You Can Do

You can't change the speed of light. But you can minimize the latency you add at your end:

- **Use fiber (FTTH)** if available — it adds the least last-mile latency.
- **Use a wired Ethernet connection** for gaming and video calls — Wi-Fi adds 1–5 ms of variable latency.
- **Choose a router with SQM/QoS** — Smart Queue Management prevents bufferbloat, the single biggest cause of home network latency spikes.
- **Pick an ISP that peers well** — an ISP with local peering to major CDNs will give you lower latency to popular services.

## The Bottom Line

The next time your ISP advertises "blazing fast 1 Gbps speeds," ask them about latency. Ask about their peering arrangements. Ask where their nearest CDN node is.

Because in the real world, the difference between a good internet experience and a frustrating one isn't about how many megabits you can download. It's about how many **milliseconds** stand between you and the server.

The speed of light is a hard limit. The best we can do is get out of its way.
