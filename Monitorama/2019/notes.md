# Monitorama 2019

- Live stream: http://youtube.com/watch?v=eZJoevaojyE

## High level takeaways / action items

- [ ] Read Lisanne Bainbridge's 1983 paper “The ironies if automation”
- [ ] Read Darrel Huff's "How to lie with statistics"
- [ ] Install and experiment with BPF for off vs on CPU traces
- [ ] Write-up strawman proposal on non-CAPA postmortems within DP/Compute

## Day 1

### Taking Human Performance Seriously In Software | John Allspaw @ (@allspaw)

### Chaos Engineering Traps | Nora Jones @ Slack (@nora_js)

- Using chaos engineering as a means to distill expertise
- Observability is “feedback that provides insight into a process and refers to the work needed to extract meaning from available data”
- "The most powerful monitoring tool is the human, lets build up that"
- "Looking at what wenr right in a chaos experiment, helps us understand what went wrong"
- Not to be seen as "Rule Enforcers"
  - Build relationships, connect people and areas of expertise
- You can get more value just going through the process of 'automating' the experiment than actually running the experiment
- Incidents are a great way to compare mental models between engineers within a given system
- Creating the chaos is easy - Thinking about safety is hard

### Observability and performance anlaysis with BPF | David Calavera @netlify (@calavera)

- How can we get the most raw data about any Linux system in production?
  - In-kernel VM to run event driven programs

    .___________________________________.
    |     Kernel     |    User Space    |
    |----------------|------------------|
    |   Verifier     |                  |
    |   BPF        Maps    BPF Program  |
    |   Events       |                  |
    .___________________________________.

  - Dont need to write C to be able to take advantage of BPF
  - github.com/iovisor/bpftrace
  - github.com/iovisor/bcc
- Flame graphs
  - On-cpu vs off-cpu flamegraphs
    - On-cpu shows when the CPU is executing syscalls, off-cpu shows when application is waiting

### The Power and Creativity of Postmortem Repair Items | Nida Farrukh (Microsoft)

- "Outages suck!"
  - We can learn to love outages?
- Post-mortems can be an avenue to argue for SPECIFIC change
  - How can we have more structured post mortems from smaller-scale outages/incidents?
- Pinpoint areas that need attention, tied to functionality that customers expect to behave
- Affect change through your repair items
  - Data collection usually the easy part, harder action is to land on specific recommended changes/repair items
  - Target different areas of focus: Detection, Mitigation, Fixes
- Timeline metric structure: Detect, Engage, Mitigate
- Questions to guide "fix" repair items
  1. "Why do we even 'X'?"
  2. Have we missed a usecase entirely during design?
  3. Can user flowers be chansge dso the same failure has less impact?
  4. Do you systems have degraded modes to switch to?
  5. Are our dependancies behaving in acordance with expectations?

### A story of one SLO | Piotr Holubowicz @Google (@holubowiczp)

- Defining SLO's for Google's 'FIFE' service after the fact
  - Challenges:
    - Multiple use cases, used by many teams
    - Implicit SLO
    - How to prioritize between different customer sizes or scenarios
    - How much to communicate broad SLO target to multiple teams
  - Ignore specific clients, focus on the scenarios
  - 

### The AWS Billing Machine and Optimizing Cloud Costs | Ryan Lopopolo

### Explain it Like I’m Five - What I Learned Teaching Observability to My Kids | Dave Cadwallader

### Automation + Artisanship: the Future of Runbooks | Kenny Johnston

### Tradeoffs on the Road to Observability | Liz Fong-Jones