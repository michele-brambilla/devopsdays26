# Taming the Metal: Platform Engineering for HPC (Ignite Talk Script)

## Part 1: Introduction

### Slide 1: Taming the Metal
  * Visual Suggestion: A high-impact photograph of the Alps supercomputer cabinets featuring the prominent blue "ALPS" logo and mountain graphics.
  * Script: This is a story about Taming the Metal. We were standing at the foot of Alps—not just a mountain in Switzerland, but one of the world's most powerful supercomputing infrastructures.
  
### Slide 2: The assumption
  * `Platform Engineering assumes your infrastructure is in the cloud.` What if there is no cloud? What if it's 10,000 bare-metal nodes?
  
### Slide 3: The Peak
  * Visual Suggestion: A high-impact photograph of the Alps supercomputer cabinets.
  * Script: Alps is a titan of infrastructure, housing 2,688 GH200 nodes linked by Slingshot-11. With 200 Gbps injection bandwidth, we've forged a platform where massive peak performance meets the low-latency demands of global science.
  * Script: Alps is a beast of pure performance. It’s built for massive scale, extreme speed, and precision. But like any high-altitude peak, it is an environment that is naturally cold, rigid, and unforgiving

### Slide 3: One Hardware, Many Worlds
  * Visual Suggestion: Icons showing MeteoSwiss, User Lab, ML/AI workloads.
  * Script: One problem: MeteoSwiss needs weather forecasts. Researchers need HPC clusters. AI teams need GPUs. Different workflows, different SLAs, same hardware."
  
### Slide 4: The complexity
  * In the traditional HPC world, the metal is king. Everything is optimized for the hardware. This means static configurations, manual setups, and a 'gatekeeper' culture where every change requires a ticket.  

### Slide 5: Introducing vClusters
  * Visual Suggestion: The "High-level Architecture" hand-drawn sketch showing Platforms, vClusters, and Infrastructures.
  * Script: We’ve revolutionized our architecture using vClusters. By abstracting the infrastructure, we partition massive systems into logical platforms. This allows us to operate diverse workloads—from WLCG to ML—using one consistent, automated methodology. (REVIEW)

### Slide 6: The Challenge
  * Script: This was our mountain. We had to find a way to bring Platform Engineering—the art of making infrastructure invisible—to an environment that was never designed to be hidden or flexible. And this is the story of how we get on top of it.
  
  
## Part 2: the story 

### Slide 7: The Era of Manual "Metal"
  * Script: Our Ops team was small but dedicated. They lived in a world of manual Ansible playbooks, often stored on individual machines. Every change was a bespoke operation, a handcrafted fix for a rigid beast

### Slide 8: The Bottlenecks
  * Script: We hit several walls: only a few engineers knew the secrets of each cluster, building images with the vendor-provided system was a tedious black box, and system boots took ages. Changes required long-lead scheduling

### Slide 9: The Ivory Tower (Solution) Seduction
  * Script: We created a pure Dev team to build an alternative. For two years, we engineered a solution. It was technically brilliant but remained on the shelf—miles away from the reality of production

### Slide 10: The Great Dualism
  * Script: A friction emerged. Ops preferred the reliability of the 'old way' they understood, while Devs had a solution no one knew how to operate. The wall between them was higher than the Alps

### Slide 11: The Merger
  <!-- * Visual Suggestion: Two separate paths converging into a single, strong highway leading toward the mountains. -->
  * Script: When the status quo became unbearable, we merged the teams. In a couple of months, not years, we pushed through staging into production. We found the bugs together, fixed them, and finally started taming the metal.

  
## Part 3: tech stack

### Slide 12: The Accidental Blueprint
  * Visual Suggestion: A professional Platform Engineering reference diagram (like the one in source) with a hand-drawn "CSCS Architecture" sketch overlaid on top of it.
  * Script (34 words): "We didn’t start with a blueprint or a Platform Engineering handbook. We had a mountain of hardware and a DevOps mindset. Only later did we realize our solution mapped perfectly to industry standards."
    
### Slide 13: The Delivery Plane (IaC)
  * Visual Suggestion: A GitLab CI/CD pipeline visual showing a "Green" success state, next to a Terraform logo and code snippets from a main.tf manifest.
  * Script (34 words): "Our Delivery plane is pure code. We use GitLab pipelines and Terraform to define everything. Changes aren't manual operations; they are validated commits in Git, ensuring our bare metal behaves like software."
    
### Slide 14: The Orchestration Engine
  * Visual Suggestion: A split visual: Nomad managing tasks on compute nodes and ArgoCD managing the services plane (Helm charts/Pods).
  * Script (35 words): "Every platform needs an orchestrator. We use a two-pronged approach: Nomad schedules tasks directly on bare-metal compute nodes, while ArgoCD manages the services plane. Together, they turn complex hardware into manageable resources.
  
### Slide 15: vServices: The Resource Plane
  * Visual Suggestion: Modular "vService" blocks (Slurm, ML tools, IAM) stacking on top of a "Generic OS Image" base layer.
  * Script (34 words): "In the Resource plane, we decoupled the user environment from the hardware. Modular vServices allow scientific communities to deploy tailored stacks—from AI to Slurm—on top of a single, generic OS image."
    
### Slide 16: The DIY Potential 
  * Visual Suggestion: A high-quality image of an open, professional toolkit or a "Construction Zone" sign where the workers are the users themselves.
  * Script (34 words): "The power of this platform is its openness. In principle, any community can now write their own vServices and bring their own environment. While not yet fully embraced, the toolkit for DIY self-service is ready."

## Part 4

###  Slide 17: The Production Reality (Sort of Nailed It)
  * Visual Suggestion: A "Green" dashboard showing active production metrics, but with a small, humorous "Under Construction" icon in the corner.
  * Script (34 words): "We sort of nailed it. Today, 16 vClusters run in production, delivering millions of CPU hours. We hit our 95% availability target for production workloads, proving that platform engineering on bare metal works."
      
### Slide 18: Shifting the Culture
  * Visual Suggestion: A graphic showing a heavy "Ticket" being replaced by a sleek "Merge Request" icon.
  * Script (33 words): "It wasn't just a technical win; it was a cultural one. We moved from 'opening a ticket and waiting' to opening an MR. We dramatically reduced toil, giving our admins visibility and autonomy

### Slide 19: The Maloja Pass
  * Visual Suggestion: A scenic photograph of the winding Maloja Pass mountain road to symbolize the technical journey.
  * Script: Navigating the Maloja Pass is the perfect metaphor for our journey. We have mastered technical curves—from storage struggles to cultural shifts—reaching the summit by embracing automation and modern Platform Engineering principles.

### Slide 20: The View from the Top is the Next Mountain
  * Visual Suggestion: A wide-angle shot from a mountain peak looking toward a much higher, distant peak labeled "vServices 2.0."
  * Script (35 words): "But the view from the top is just the next mountain. To overcome current limitations and reach complete automation, we are already building vServices 2.0. The beast is tamed, but the journey continues."
