# Monitorama 2018

## High level takeaways / action items

- [ ] Start to outline onboarding system for new SREs
- [ ] Build on-call simulator for new engineers, help learn the environmenty in low-stakes scenario with real-world situations
- [ ] Think through achievable projects for new engineers
- [ ] Starting building anything you're learning as soon as possible!
- [ ] Think through how we can enable Slack-Bots to increase productivity
- [ ] Build context into alerting (Docoumentation? Past similar events? Query for recent changes?)

## Day 1

#### Logan McDonald @loganmeetsworld - BuzzFeed - Optimizing for Learning
- "Problem solving is easier with constraints"
    - Dickerson Hierarchy of SRE
- Build as soon as possible!
- Make information open and available, enables new hires to onboard quickly
- "Dont Google it! ...yet"
    - Low stress retreival helps build long term memory
- To learn, struggle
- Mental models
    - Events > Patterns > Structure (Abstractions)
- Reflection KEY!
    - Incident reviews, focus less experienced engineers on attending
- Pyschological safety
    - Safe to ask any question!

### Pam Selle @pamasaur - IOPipe - Serverless and CatOps
- "What problem do you want to be solving?"
    - Server config/patching/security/etc
- "If youre not using an event driven system, serverless not for you"
- Know the limits of the system

### Mentoring Metrics Engineers - Yelp - Zach Musgrave / Angelo Licastro
- Forcing functions for sharing knowledge
    - Mentor/mente meetings - No silly questions!
- Make sure projects are achievable for interns/mentees!
- Act as consultant for feature teams
    - Self service!
    - Documentation

### Dawn Parzych - Catchpoint - The Power of Storytelling
- Storytelling - Keep It Simple Stupid!
    - Easy to overcomplicate
- Much more difficult to make an impact in work and in life without narrative
    - Build context! Build a story!

### Jamie Wilkison - A Treatise on the Metrology of Service Level Objectives
- Symptom Based Alerting
    - Anything that can measured by the SLO
- Start with identifying what you want to measure, not the measurments themselves
    - SLI (Indicator) - a carefully defined quantitative measure of some aspect of the level of service that is provided
    - SLO (Objective) - a target value or range of values for a service level that is measured by an SLI
    - SLA (Agreement) - an explicit or implicit contract with your users that includes consequences of meeting (or missing) the SLOs they contain


### Franka Schmidt - On-call Simulator! - Building an interactive game for teaching incident response
- On-call Onboarding
- Buddy system
- Bucket List
    - 1. Anytime
    - 2. Depends on workload
    - 3. May need to involve someone else
- On-Call Simulator Game 
    - Pick software (Twin light weight easy to use)
    - Find scenarios that new engineers can step through
    - Pick 


### Peter Bourgon - Observability: the Hard Parts

### Aditya Mukerjee (@chimeracoder) - Warning: This Talk Contains Content Known to the State of California to Reduce Alert Fatigue
- Improve on-call rotations
- Executive functioning skills
- "If it's unclear who should be taking action, the alert is *not actionable*"

### Ian Bennett - @enbnt - Monitory Report: I Have Seen Your Observability Future. You Can Choose a Better One.
- Watch 2016 video on Mon 2.0 from Twitter!

## Day 2

### Kishore Jalleda - Want to solve Over-Monitoring and Alert Fatigue? Create the right incentives!

### Peter Bailis - Next-Generation Observability for Next-Generation Data: Video, Sensors, Telemetry

### Aruna Sankaranarayanan (Mapbox) - Coordination through community: A swarm of friendly slack bots to improve knowledge sharing
- Small team, no documentation for a small team
    - Was using "Learn as you go" system
- Had timezone gap between US/India, had to rely heavily on documentation
- On-call onboarding & setup
    - Buddy system (3 months)
        - Phase 1 (1 Month)
            - Shadowing the primary engineer, mostly passively
        - Phase 2
            - Taking incidents together with buddy, but driving and handling smaller tasks
        - Phase 3
            - Taking incdients primarily, with bddy available for help if needed
- Monitoring system
    - Sumologic
        - Distributed logging/metrics platform
- Slack
    - Increases visibility
    - Timezone independant, easy to consume independently
    - Allows for more eyes on problems, and involves more junior engineers and support folks where they otherwise wouldnt be
- Slack bots
    - Help drive down the noise
    - Each bot Lambda function
        - @mapbox <command> <options>
    - Help increase visibility
        - SumoLogic queries
            - Used bot to make sumo queries simpler, and allows engineers who dont know the query language to interface with sumo

### Andy Domeier (SPS Commerce) - Automate Your Context
- https://github.com/adomeier/OperationalReadiness
- Value velocity / performance
    - Companies that ship faster, generally are succeeding
- Complexity stresses the need for context
    - Ask the right kinds of questions
    - Create a culture of curiosity
- Operational Readiness
    - A base set of consistent values for service delivery give you context about the app and enables you to make decisions
        - Operations Information
            - Who?
            - Where?
        - Performance
            - KPIs
            - Cost
        - Agility
            - Change effectiveness
            - Architecture & Resilliancy
        - Security
            - Sounds cool!

### George Luong (Slack) - Slack in the Age of Prometheus
- 