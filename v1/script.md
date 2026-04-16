# Full Script – 20 Slides

## SETUP (Slides 1–3)

### Slide 1: Taming the Metal
**Visual:** High-impact photograph of Alps supercomputer cabinets with blue "ALPS" logo.

**Script:**
"This is a story about Taming the Metal. We were standing at the foot of Alps—not just a mountain in Switzerland, but one of the world's most powerful supercomputing infrastructures. 2,688 GPU nodes. 200 Gbps injection bandwidth. Pure performance. But like any high-altitude peak, it's cold, rigid, and unforgiving. And we had to figure out how to make it work."

---

### Slide 2: One Hardware, Many Worlds
**Visual:** Three icons/logos: MeteoSwiss, Research Lab, AI/ML team. All pointing to the same hardware.

**Script:**
"Here's the problem: one machine serves three completely different masters. MeteoSwiss needs it for weather forecasts with tight SLAs. Researchers need flexible HPC clusters. AI teams need GPUs for training. Different workflows. Different demands. Same hardware. And nobody agreed on how to run it."

---

### Slide 3: The Silos
**Visual:** Two tall walls separating "Ops" on the left from "Devs" on the right. Hardware at the base.

**Script:**
"Behind that hardware challenge was a human one. Our Ops team owned the metal—they understood the hardware, the networking, the bare-metal reality. Our Dev team built solutions—automation, orchestration, modern tooling. But they lived in separate worlds. Changes required hand-offs. Tickets lived in limbo. And nothing moved fast."

---

## CONFLICT (Slides 4–7)

### Slide 4: The Old Way
**Visual:** A tangled mess of Ansible playbooks, sticky notes, handwritten documentation. Maybe a single server rack in shadow.

**Script:**
"Our Ops team was small but dedicated. They lived in a world of manual Ansible playbooks—often stored on individual machines. Every change was bespoke. Every fix was handcrafted. The hardware was king, and everything else bent to its will. Flexibility? That wasn't part of the vocabulary."

---

### Slide 5: The Bottlenecks
**Visual:** Three bottleneck illustrations: a narrow hourglass, a door with a line of people, a calendar marked with X's.

**Script:**
"We hit walls everywhere. Only a few engineers knew the secrets of each cluster—knowledge lived in their heads. Building images with vendor-provided tooling was a black box nightmare. And system boots took hours. Every change required long-lead scheduling. Every ticket was a negotiation."

---

### Slide 6: The Breaking Point
**Visual:** A crashing wave, or a mountain peak surrounded by storm clouds.

**Script:**
"Then the status quo became unbearable. Teams were waiting weeks for simple changes. The hardware was incredible, but we couldn't use it. Ops was drowning in manual work. Devs were frustrated. Something had to give. And it did."

---

### Slide 7: The Ivory Tower
**Visual:** A tall, isolated tower on a hilltop. Fancy but disconnected from the ground.

**Script:**
"We created a pure Dev team to build an alternative. For two years, we engineered a solution. It was technically brilliant—modern, elegant, everything we thought we needed. But it stayed on the shelf. Nobody knew how to operate it. It was miles away from the reality of production."

---

## TURNING POINT (Slides 8–9)

### Slide 8: The Merger
**Visual:** Two paths or rivers converging into one strong stream flowing toward mountains.

**Script:**
"When the ivory tower failed, we did something radical. We merged the teams. Ops and Devs became one unit. Not in name only—in practice. They sat together. They owned problems together. In a couple of months—not years—we pushed through staging into production. We found the bugs together, fixed them together, and started taming the metal."

---

### Slide 9: DevOps Mindset
**Visual:** A circular diagram showing "Code," "Infrastructure," "Operations," all flowing together. Or just the words overlapping.

**Script:**
"What changed wasn't just org structure. It was mindset. Infrastructure became code. Code became infrastructure. Operations became automation. There was no 'throw it over the wall'—everyone owned the outcome. And with shared ownership came shared urgency and shared accountability."

---

## SOLUTION (Slides 10–15)

### Slide 10: One Team, One Workflow
**Visual:** A Git commit log, or a merge request interface. Shows multiple authors (Ops and Dev names mixed).

**Script:**
"The foundation was Git. Everything lived there. Not just application code—infrastructure, configurations, deployments. When Ops and Devs speak the same language—Git—magic happens. Pull requests become the conversation. History becomes transparent. And there's nowhere to hide a bad change."

---

### Slide 11: Delivery as Code
**Visual:** Split screen: GitLab CI/CD pipeline (showing green checkmarks) on the left, Terraform code snippets on the right.

**Script:**
"Our delivery plane is pure code. GitLab pipelines validate every change. Terraform defines every resource. No more 'I'll run this command on the server.' No more mystery. Every infrastructure change is a commit, reviewed by the team, tested in CI, deployed by automation. The bare metal behaves like software."

---

### Slide 12: Orchestration Engine
**Visual:** Split visual: Nomad managing compute nodes on the left, ArgoCD managing services/pods on the right. Arrows connecting both to the hardware.

**Script:**
"Every platform needs an orchestrator. We use two: Nomad schedules tasks directly on bare-metal compute nodes—no abstraction layer getting in the way. ArgoCD manages the services plane—Kubernetes, containers, all the modern tooling. Together, they partition one massive machine into many logical platforms without teams stepping on each other."

---

### Slide 13: vServices: Environments on Demand
**Visual:** Modular stacked blocks labeled "Slurm," "ML Tools," "Storage," "IAM," all stacking on top of a "Generic OS Image" base layer.

**Script:**
"In the resource plane, we decoupled the user environment from the hardware. We call them vServices—modular, reusable software stacks. A research team writes a vService that includes Slurm and their libraries. An AI team writes one with PyTorch and training tools. They deploy on top of the same generic OS image. Same hardware, different worlds. No silos."

---

### Slide 14: One Hardware, Many Platforms
**Visual:** A high-level architecture diagram showing the bare-metal layer at the bottom, then vClusters on top, then different user communities (MeteoSwiss, Research, AI) using different vClusters simultaneously.

**Script:**
"Here's how it all connects. We have 10,000 bare-metal nodes. On top, we run 16 vClusters—logical partitions, each with its own orchestration, its own resource model, its own SLAs. MeteoSwiss gets one. Researchers get another. AI teams get another. One machine. Many platforms. One workflow. That's the architectural win."

---

### Slide 15: The DIY Toolkit
**Visual:** A professional toolkit, or construction site with builders. Caption: "Users write their own vServices."

**Script:**
"The power of this architecture is that it's open. In principle—and increasingly in practice—any scientific community can now write their own vService and bring their own environment. They're not waiting for Ops to hand-craft a solution. They're building it themselves. This is what breaking silos actually looks like: users have agency."

---

## RESULTS (Slides 16–18)

### Slide 16: Production Reality
**Visual:** A green dashboard showing metrics: 16 vClusters, 95% uptime, number of CPU hours shipped. Include a small "Under Construction" icon or humor.

**Script:**
"We didn't solve everything. But we shipped. Today, 16 vClusters run in production, delivering millions of CPU hours to research and weather forecasting. We hit our 95% availability target for production workloads. We proved that platform engineering on bare metal works—if you solve the human problem first."

---

### Slide 17: Cultural Shift
**Visual:** Before/after: Heavy "Ticket" icon on the left, replaced by sleek "Merge Request" icon on the right. Show the change.

**Script:**
"It wasn't just a technical win. It was cultural. We moved from 'open a ticket and wait' to 'open a merge request and ship.' We dramatically reduced toil. Our admins went from firefighting to building. And—this matters—they had visibility and autonomy. They weren't gatekeepers anymore. They were enablers."

---

### Slide 18: What Actually Worked (and What Didn't)
**Visual:** Two columns: "Worked" (green checkmarks) and "Still Hard" (yellow caution signs).

**Script:**
"Let's be honest. Unifying the teams worked. Git-based workflows worked. Automation reduced toil. But self-service vServices? Still emerging. Some communities embraced it; others still ask Ops. We're not done. The beast is tamed, but it's not fully domesticated. And that's okay—we have momentum."

---

## FUTURE (Slides 19–20)

### Slide 19: What's Still Hard
**Visual:** A mountain peak with a higher peak visible in the distance. Or a partially constructed bridge.

**Script:**
"We still struggle with some things. Multi-tenancy gets complex. Resource isolation isn't perfect. Cost attribution is fuzzy. Building and maintaining vServices takes effort—we don't have a library yet, just individual solutions. And not every team has embraced self-service. These are the Maloja Passes ahead—technical curves we have to navigate."

---

### Slide 20: The Next Mountain
**Visual:** A sweeping vista from a mountain peak, with a much higher, distant peak labeled "vServices 2.0" or "Complete Self-Service."

**Script:**
"But the view from the top is just the next mountain. We're building vServices 2.0—better templating, clearer SLAs, real cost models. The goal is radical self-service: communities define their entire stack, deploy it themselves, pay for what they use. No silos. No gatekeepers. The real taming of the metal. We're not there yet. But we're climbing."

---
