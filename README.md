---
title: "Starter Marp Slides"
marp: true
paginate: true
theme: cscs
size: 16:9

---

<!--
_class: titlecover
_paginate: skip
-->

# Taming the Metal: Platform Engineering for HPC

### Michele Brambilla, CSCS

##### DevOpsDays Zurich 2024
---

# Welcome

- This is a starter Marp slide deck.

---

## Example Slide

- Add your content here.

---


---

<!-- _class: platform-overview -->
# Platform Engineering

<div class="platform-grid">
  <div class="platform-card">
    <h3>Golden Paths</h3>
    <p>Reduce cognitive load.<br>Pre-paved routes for developers.</p>
  </div>
  <div class="platform-card">
    <h3>Self-Service</h3>
    <p>Teams provision what they need, when they need it.</p>
  </div>
  <div class="platform-card">
    <h3>Internal Platform</h3>
    <p>One product serving all engineering teams.</p>
  </div>
</div>

<!-- bottom-left attribution -->
<div style="position:absolute;left:10%;bottom:20%;z-index:3;font-size:1.6vh;color:currentColor;opacity:0.85">platformengineering.org</div>

---

# The Assumption

> "Platform Engineering assumes your infrastructure is in the cloud."

<div style="margin-top:18px;padding:18px;background:#213a50;border-left:6px solid #d9571a;color:#ffb39b;">What if there is no cloud? What if it's 10,000 bare-metal nodes?</div>

---

<!-- _class: alps -->
# Alps — The Supercomputer

<div class="platform-grid alps-grid">
  <div class="platform-card">
    <div class="stat-value">434.9</div>
    <div class="stat-label">Petaflops</div>
    <div class="stat-note">sustained peak</div>
  </div>
  <div class="platform-card">
    <div class="stat-value">10</div>
    <div class="stat-label">Exaflops</div>
    <div class="stat-note">BF16 (AI)</div>
  </div>
  <div class="platform-card">
    <div class="stat-value">2,688</div>
    <div class="stat-label">Nodes</div>
    <div class="stat-note">Grace-Hopper GPUs</div>
  </div>
  <div class="platform-card">
    <div class="stat-value">4</div>
    <div class="stat-label">Sites</div>
    <div class="stat-note">Lugano · Lausanne · PSI · ECMWF</div>
  </div>
</div>

<div style="margin-top:18px;padding:14px;border-radius:4px;text-align:center;">HPE Cray EX · Slingshot-11 Interconnect (200 Gbps/node) · 100+ PB storage</div>

---

# One Hardware, Many Worlds

<div class="platform-grid one-hardware">
  <div class="platform-card">
    <div class="stat-label">MeteoSwiss</div>
    <div class="stat-note">Operational weather</div>
    <div class="stat-note">forecast 24/7</div>
  </div>
  <div class="platform-card">
     <div class="stat-label">User Lab</div>
     <div class="stat-note">Research HPC</div>
  </div>
  <div class="platform-card">
    <div class="stat-label">AI/ML</div>
    <div class="stat-note">GPU-intensive</div>
    <div class="stat-note">training workloads</div>
    <div class="stat-note">inference models</div>
  </div>
  <div class="platform-card">
    <div class="stat-value">WLCG/SKA</div>
    <div class="stat-label">High-throughput</div>
    <div class="stat-note">data processing</div>
  </div>
</div>


<!-- Use HTML comments for speaker notes -->
<!-- Speaker notes: Talk about project goals -->
