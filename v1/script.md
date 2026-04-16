# Full Script – 20 Slides

## SETUP (Slides 1–3)

### Slide 1: Taming the Metal
**Visual:** High-impact photograph of Alps supercomputer cabinets with blue "ALPS" logo.

**Script:**
"This is a story about Taming the Metal. We were standing at the foot of Alps—not just a mountain in Switzerland, but one of the world's most powerful supercomputing infrastructures."

---

### Slide 2: One Hardware, Many Worlds
**Visual:** Three icons/logos: MeteoSwiss, Research Lab, AI/ML team. All pointing to the same hardware.

**Script:**
"One machine serves several masters. MeteoSwiss needs weather forecasts. Researchers need HPC. AI teams need GPUs. Different workflows. Same hardware. Nobody agreed on how to run it."

---

### Slide 3: The Silos
**Visual:** Two tall walls separating "Ops" on the left from "Devs" on the right. Hardware at the base.

**Script:**
"Our Ops team owned the metal. Our Dev team built automation. They lived in separate worlds. Changes required hand-offs. Tickets lived in limbo. Nothing moved fast enough."

---

## CONFLICT (Slides 4–7)

### Slide 4: The Old Way
**Visual:** A tangled mess of Ansible playbooks, sticky notes, handwritten documentation. Maybe a single server rack in shadow.

**Script:**
"Ops lived in manual Ansible playbooks, often on individual machines. Every change was bespoke. Every fix handcrafted. Flexibility wasn't in the vocabulary."

---

### Slide 5: The Bottlenecks
**Visual:** Three bottleneck illustrations: a narrow hourglass, a door with a line of people, a calendar marked with X's.

**Script:**
"Only a few engineers knew the secrets. Building images was a black box. System boots took hours. Every change required weeks of scheduling. Every ticket was a negotiation."

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
"We did something radical: we merged Ops and Devs into one unit. Not politics—actual unity. In 2 months, not years, we shipped to production. We broke the silo."

---

### Slide 9: DevOps Mindset
**Visual:** A circular diagram showing "Code," "Infrastructure," "Operations," all flowing together. Or just the words overlapping.

**Script:**
"What changed: infrastructure became code. Code became infrastructure. No hand-offs. One team, one problem to solve, shared accountability. That's when everything accelerated."

---

## SOLUTION (Slides 10–15)

### Slide 10: We Didn't Read a Book
**Visual:** A "Platform Engineering" textbook with a big X through it. Then show your actual solution stacked on top.

**Script:**
"We didn't know we were doing 'Platform Engineering'; we were just survivalists who built what worked."

---

### Slide 11: Git as the Bridge
**Visual:** A Git commit log, or a merge request interface. Shows multiple authors (Ops and Dev names mixed).

**Script:**
"We chose Git as the common language. Not just for code—for infrastructure, configs, deployments. Every change became a pull request. Ops and Devs reviewed together. No secrets. No hand-offs."

---

### Slide 12: Delivery as Code
**Visual:** Split screen: GitLab CI/CD pipeline (showing green checkmarks) on the left, Terraform code snippets on the right.

**Script:**
"GitLab pipelines validate every change automatically. Terraform defines resources. No manual commands on servers. Every infrastructure change is a reviewed commit. Bare metal behaves like software."

---

### Slide 13: Orchestration: No More Coordination
**Visual:** A split visual: Nomad managing compute nodes and ArgoCD managing the Kubernetes services plane

**Script:**
"Every platform needs an orchestrator. We use two: Nomad schedules tasks directly on bare-metal nodes, while ArgoCD manages the service plane. Together, they make complex hardware feel like cloud."

---

### Slide 14: vServices: The Resource Plane
**Visual:** Modular blocks (Slurm, ML, IAM) stacking on top of a "Generic OS Image" base

**Script:**
"vServices are our building blocks. By decoupling user environments from hardware, a tailored stacks—from Slurm to AI—on generic OS images can be deployed. One hardware, many software-defined worlds."

---

### Slide 15: The DIY Toolkit
**Visual:** A first-person view of a high-tech cockpit or a hand holding a "Master Key"

**Script:**
"The real breakthrough is autonomy. Cluster owners now have the keys. They don’t need to open tickets and wait; they can apply their own changes through code. The gatekeeper is officially gone."

---

## RESULTS (Slides 16–18)

### Slide 16: Production Reality
**Visual:** A green dashboard showing metrics: 16 vClusters, 95% uptime, number of CPU hours shipped. Include a small "Under Construction" icon or humor.

**Script:**
"16 vClusters in production. 95% uptime. Millions of CPU hours shipped. Platform engineering on bare metal works. But only because we solved the human problem first."

---

### Slide 17: Shifting the Culture
**Visual:** Before/after: Heavy "Ticket" icon on the left, replaced by sleek "Merge Request" icon on the right. Show the change.

**Script:**
"Cultural shifts followed. We moved from 'opening tickets' to 'opening Merge Requests.' We reduced toil, gave admins autonomy, and killed the gatekeeper model. They are finally enablers, not roadblocks."

---

### Slide 18: The Honest Truth
**Visual:** Two columns labeled "Worked" (Git, Automation) and "Still Hard" (Self-Service).

**Script:**
"et’s be honest. Unifying teams and Git automation worked. But self-service is still emerging. The beast is tamed, but not domesticated. That’s okay—we finally have the momentum."

---

## FUTURE (Slides 19–20)

### Slide 19: What's Still Hard
**Visual:** A high-quality aerial photo of the winding Maloja Pass mountain road.

**Script:**
"Navigating the Maloja Pass road is our journey’s metaphor. Mastery of technical curves—from hardware struggles to cultural shifts—reaches the summit by embracing automation and modern Platform Engineering principles."

---

### Slide 20: The Next Mountain
**Visual:** A sweeping vista from a mountain peak, with a much higher, distant peak labeled "vServices 2.0"

**Script:**
"The summit reveals the next mountain. To overcome current limitations and reach complete automation, we are building vServices 2.0. The beast is tamed, but the journey continues. Thank you."

---
