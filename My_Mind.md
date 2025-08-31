This is like my diary to be able to read my innter thoughts. Ill update it fequentry with steps and updates as i see fit.


# Inspiration  

This is a project I am currently working on. I recently got a job as a Cyber Security Analyst, but instead of jumping straight into success, we spent a lot of time in training. Constantly I asked myself: *why is there so much training?* Obviously this is an incredibly important job and it isn’t something you can just hand to anyone.  

During training, I found myself wanting something more hands-on. Reading frameworks and studying GRC concepts is useful, but it can feel mind-numbing. How do you even know if you’ll enjoy the job if you can’t really practice it until you’re already in the role?  

This is the reason for this lab.  



## What I’m Wanting to Accomplish  

This is a lab designed to practice being, in many ways, a Cyber Security Engineer. I want it to be extremely versatile and give you a little bit of everything. The lab will simulate different types of companies and will show that GRC is not a one-size-fits-all solution. Instead, GRC adapts to each company, requiring tailored controls and policies to deliver the best possible outcomes.  

 

## How I Am Going to Do It  

The lab will provide every step, depending on how much the student wants to do. I will create enterprise infrastructures that can be **downloaded prebuilt**, or **created manually** if someone wants a full hands-on experience.  

 

## Beginning Steps  

- **Using Proxmox** – This is the main hypervisor I’ll use. It’s similar to ESXi and other enterprise hypervisors, so the skills translate well.  

- **Using VMware/Hyper-V/VirtualBox** – I may also explore this route. If I go this way, I’ll provide VM images and possibly set up a web server where students can download them. For now, I may use VMware Pro since it’s free to download.  

### Problems  

- This project is extremely hardware-intensive. Right now I’m using a ~$1000 server from the internet, but there are cheaper options out there. The resource cost is something I’ll need to keep working on.  
- Since this project will use Windows, there may be issues when uploading/sharing Windows images that aren’t official distributions. This could disrupt the “public” student project side and turn it into a personal-only project. I need to investigate licensing and distribution further.  
- **Scalability** may be a challenge long term. Running this on a single Proxmox box works for me, but if students need dozens of VMs, or if this ever grows into a public training environment, cloud hosting or lightweight container-based builds may need to be explored.  

 

## Infrastructure  

- **pfSense** for firewalls and routing.  
- **Windows 11** images for workstations.  
- **Windows Server 2022** for Active Directory and Group Policies.  
- An **IT/Security workstation** with SIEM, IDS/IPS, and threat detection.  
- Multiple virtual switches and routers, ideally with redundancy to mimic real-world design.  
- Possible additional servers: **Backup server, WSUS (update server)**, etc.  

### Problems  

- I don’t have a clear “real-world” enterprise infrastructure map since most companies don’t share these details. I may need to research open resources or reach out to professionals.  
- Integrating all configuration files in a way that students can easily set up may be difficult. Some students don’t like networking and just want to practice the security/policy side, so I need to design it in layers (infrastructure vs. compliance).  

 

## Plan for the Lab Once the Infrastructure is Done  

- Each VM will have a **page describing its problems** (e.g., not joined to the domain, weak screensaver settings, misconfigured GPOs, bad firewall rules, etc.).  
- Since Active Directory ties everything together, students can either:  
  - Log into each VM individually and hunt for problems, or  
  - Scan through the GPOs and configurations to identify issues from a central point.  
- I’ll also include **cheat sheets** for each machine with known issues and remediation guidance.  
- Problems will come in **phases**:  
  - **Networking students** → focus on connectivity and misconfigurations.  
  - **Security/GRC students** → focus on policies, controls, and remediation.  
  - **Snapshots will exist for different stages** → for example, one snapshot will have networking issues in place, but if a student doesn’t want to deal with networking, they can skip ahead to the “fix lab” snapshot and jump straight into the compliance and security side.  

### Problems  

- Will this be too difficult? Some students may not be able to recognize issues they’ve never seen before. I’ll need to test this with real students to make sure it’s feasible.  
- **Metrics for success** are tricky. Maybe a checklist could be used, but even if students complete framework mappings, there’s no guarantee they implemented them correctly. The real measure will be comparing their results with other students, and documenting their process clearly.  
- **Instructor mode** might be needed eventually. Something like an answer key or teacher guide so an instructor can evaluate work. I’m not planning this now, but it’s worth noting.  

 

## Scenarios  

- Each company type will need **building layouts and schematics** to simulate a real business.  
- I don’t like fictional companies that are too “perfect.” I want hands-on remediation and real issues to deal with. For this reason, I’ll provide as much company context as possible (locations, industry details, processes) so students can make accurate RMF sheets and give realistic advice.  
- These scenarios will eventually be tied to **specific industries and physical locations**, so students understand the **unique compliance requirements and risks** of each environment. For example:  
  - Financial company → PCI-DSS, insider threat, access control  
  - Aerospace company → ITAR/CMMC, export controls, engineering data protection  
  - Logistics company → supply chain risks, downtime impacts  
  - IT/OT company → SCADA/ICS, segmentation between IT and industrial networks  

### Problems  

- This can get subjective, and I may make mistakes. I might need a professional to review my work, but that’s a big time ask.  
- Can I even share building schematics or make my own realistically? That’s still a question.  
 

## Frameworks  

- NIST CSF  
- NIST RMF (SP 800-37)  
- CMMC  
- NIST SP 800-53  
- NIST SP 800-171  

### Problems  

- Not sure yet if students will just be running gap analysis, writing policies, or both. This part needs clarity.  

 

## Remediation  

- Students should create a **remediation document** as part of their RMF policy manual, then implement their changes.  
- They should have a way to **share their work** (LinkedIn posts, GitHub repos, maybe even walkthrough videos).  
- This will be documented as if they are **real Cybersecurity Analysts**. Students should practice not just fixing problems, but also communicating fixes clearly in writing and presentations.  
- **Student Guidebook** – I’ll include a README-style document as a guidebook for students to get started. This will cover setup, expectations, and how to approach the lab.  

### Problems  

- None identified yet, but I’m sure more will come up as the project grows.  

 

## ChatBot  

The chatbot will simulate conversations with a **non-technical company representative**. This person won’t know terms like GPOs, segmentation, or RMF. They’ll speak in business language or misunderstand technical details, forcing students to practice communication skills.  

### Problems  

- I still need to figure out how to implement this. Options include:  
  - Custom ChatGPT prompts.  
  - A lightweight web app with a chatbot.  
  - Self-hosted AI (but this requires more compute power).  
  - AWS-hosted bot with pay-per-use.  
- I also need to test whether AI can convincingly play this role (confident but not technical).  

 
