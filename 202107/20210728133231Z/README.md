#  Key takeaways from the devops reports for 2020

## Devops Institute report
>  https://www.bmc.com/content/dam/bmc/collateral/third-party/2020-Upskilling-Report-FINAL.pdf

Generally, we have pretty advanced technology, but it is important to also improve soft skills, as they are just as important

Digitalization is said to be the Fourth Industrial Revolution

At first devops were more about the technical requirements, now that we surpassed this barrier, it has now become about human skills, process, governance and such

Compared to 2019:
- devops engineers role title doubled in popularity
- hiring is largely done through external recruiters
- Agile, Devops and ITIL are being challenged by SRE practices (adoption wise)
- performance tuning and monitoring have risen in must-have skills
- the Hybrid DevOps have risen in demand, requiring an holistic view of the devops workflow, including human, process, knowledge and automation skills
- Where before it was more about being specialist in one field(T shaped), now it is about the E shaped, where you need to have a broad knowledge and be specialist in many skills
  - the three specialties include: automation, functional skills and technical skills
- certifications are not as important as:
  - process skills and knowledge
  - automation skills
  - soft skills
- certifications are more important for contractors than it is for other roles, such as IC, C, or Mgmt levels

The DevOps human must have functional skills which include:
- IT Operations (ITOps)
- security practices
- IT infrastructure
- application development and design (AD&D)
- quality assurance
- business continuity disaster recovery (BC/DR)

CI/CD was asked for the first time and clearly it became the most voted as
must-have skill, followed by actual public cloud knowledge, analytical
knowledge, programming languages, and so forth

## Redgate report
> https://assets.red-gate.com/solutions/database-devops/state-of-database-devops-2021.pdf

NoSQL has come to stay, over 47% of respondents use NoSQL

Key findings of the report include:
- Among software delivery performance clusters, the Elite and High performers are
more likely to have implemented DevOps and Database DevOps practices.
- On average, Elite performers are also considerably faster in delivering database
changes.
- Large enterprises are more likely to have adopted DevOps than smaller ones, and
so are industries such as high-tech and financial services.
- Cloud adoption showed a drastic acceleration, with only one in five respondents
hosting databases only on-premises.
- We saw a significant increase of estates with diverse database technologies from
61% in 2020 to 70% in 2021.
- Overall, the Covid-19 pandemic has had moderate impact on performance and
productivity for most IT teams. In fact, with remote working, individual productivity
has actually improved for the majority (63%).
- The majority of respondents (68%) expect the budget for database management
and tooling to stay at least the same or increase in the next 12 months, indicating
the importance of it within the overall IT strategy.

Obstacles o DevOps implementation (ordered)
- lack of skill in the team
- disruption to existing workflow
- lack of alignment between dev and ops team
- lack of awareness of the benefits to the business side
- lack of budget for new tooling
- lack of support from executive leadership

Automation is key to improve software delivery and Ops performance (CI/CD)

## Puppet report
> https://media.webteam.puppet.com/uploads/2021/07/Puppet-State-of-DevOps-Report-2021.pdf

- Evolved, highly developed SRE/Devops teams have a clear understanding of the
responsability of their team
- Cultural blockers are what mostly hold back DevOps advancements


DevOps might have reached a point where teams aren't even saying they are doing
DevOps anymore, it is just how they work

> "DevOps is whatever you do to bridge friction created by silos, and all the rest
> is engineering"
_Patrick Debois, ADvisor, Snyk (Formerly DevOpsDays)_

Historical movement: SysAdmins become devops, with an increase in salary
attached, and now DevOps are becoming SREs, with the same income increase
happening again.

Known definitions for "DevOps":
- team with end-to-end responsabilities (Dev and Ops together)
- team who supports Dev team with release automation, deployment pipelines, and
  developer tooling
- team who develops and mantain things developers don't want to care about:
  infrastructure, container fabrics, monitoring, metrics.
- team who encourages DevOps practices across the organization

> The lack of clarity of amount of ways DevOps teams can work is a barrier for
> performance, as, for a fact, having clear reponsabilities  helps to increase
> the team performance, and also help those who interact with team to understand
> exactly what the DevOps team is supposed to do. So moving away from the
> "DevOps" teams to more clear roles is advised, such as: "Platform
> Engineering", "Tooling Team", "Observability Team".

For high-adoption teams, the biggest blockers are:
- legacy architecture
- lack of skilled workers
both of which would fade out as time goes by

Use of internal platforms has a high correlation with DevOps evolution within a
firm

> Create guardrails that reduce burden and enable agility

__Four Fundamental Topologies__
- Stream-aligned team: Aligned to a flow of work from (usually) a segment of the
  business domain.
- Enabling team: Helps a stream-aligned team to overcome obstacles. Also detects
  missing capabilities.
- Complicated subsystem team: Where significant mathematics/calculation or
  hard-to-find niche technical expertise is needed full-time.
- Platform team: A grouping of other team types that provide a compelling internal
  product to accelerate delivery by stream-aligned teams.

> Most of the companies I have contact with, I have filled a role in the
> Stream-aligned team

__Three team interaction modes__
There are only three ways in which teams should interact:
- Collaboration: Working together for a defined period of time to discover new
  things (APIs, practices, technologies, etc.).
- X-as-a-Service: One team provides, one team consumes something “as a Service.”
- Facilitation: One team helps and mentors another team.

Known high performant teams tend to have teams focused on tooling, and teams
focused on developing internal tools, end-to-end

It is not just about automation
- cannot focus on automation to the detriment of team interaction, fast flow,
  collaboration and optimization
- usually easier to focus on technical stuff such as automation instead of
  discussing the points above which requires talking to larger scopes
- automate repetitive tasks, and make as much as you can self-service

Public clouds made provisioning of resources much quicker, but it goes further
than just Infrastructure-As-Code for a server, we need to leverage the cloud by
making as much as we possible be self-service, automating other repetitive tasks
such as config management, monitoring, overall trying to reduce cognitive load
while empowering development teams. As, besides being able to quickly provision
resources, the cloud also allows to easily do management tasks on them.

DevOps and Security experience usually equals to higher salary

Reaching higher levels of DevOps adoption is usually attached to having
successfully implemented a platform team approach, with well-defined team
responsabilities and interactions, buy-in from managers and users, strong
automation practice and willingness to accept risk.

Among highest blockers for breaching from mid-high to high level:
- insufficient feedback loops
- unclear responsabilities
- failure to share best practices
notice none of the above is necessarily technical

Among highest blockers for breaching from mid-low to high level:
- skill shortage
- legacy architecture
- resistance to change
- lack of automation
mid-low teams already have some DevOps practices in-place but are still facing
many of the challenges of those with low level DevOps adoption

> Stating blockerrs as "cultural" can lead to inaction as people think of
> culture as "immutable" or very hard to change

> Highly evolved firms make heavier use of internal platforms for their engineers,
> enabling developers to access authentication (62 percent), container
> orchestration (60 percent), and service-to-service authentication (53 percent),
> tracing and observability (49 percent), and logging request (47 percent)
> services via self-service

> The last thing you want is to have your developer team ask you for
> something and you don’t have it for them. It’s essential to think of
> the things you build as products, you should always have a proof
> of concept. This is core to DevOps, even if your proof of concept
> fails, you built it, you tried it, you learned.
> _Katharine Yi, Senior Cloud Engineer at Arena Analytics_

DevOps might be moving into a more consultative role, where they act more like
"enablers" and "force multipliers"

> Collaboration is expensive. If you need to have real-time discussion and work
> to get something done, you’ve effectively reduced output by the number of
> parties involved in that collaboration.

> The reasons that collaboration is required are just as
> important as the type of collaboration.

> Make the right things easy and the
right things will happen quickly.

## Extra takes from resources referenced in the reports

### The Three Ways: Principles underpinnin DevOps
> ref: https://itrevolution.com/the-three-ways-principles-underpinning-devops/

1. Systems Thinking
  - understand flow of work (eg.business > dev > ops > client)
  - don't allow defects to be move downstream or backwards
  - seek to increase flow
    - need to track re-work to find bugs and opportunities for optimization
  - never sacrifice local optimization for global degradation
2. Amplify Feedback loops
  - Once automation is in-place you will start finding opportunities for more
    feedback loops
  - With more iterations, you promote better understanding of the system, reduce
    toll and make sure it becomes progressively better
3. Culture of Continual Experimentation and Learning
  - promoting a culture that experiments, takes risks and learns from failure
    - calculated risks with proper risk assessments and recovery plans
    - will inevitably increase system resillience
  - repetition and practice will become mastery

__Personal takeways:__

To help DevOps adoption, understand the complete flow of the work, and define
it, put automation where possible, in order to increase feedback loops and
gradually improve the pipelines, promote a culture of risk taking and learning
from failure, will promote proper ownership by the team, keep good track of work done
to be able to assess bottlenecks, opportunities for improvement and so forth


## Actionable takeaways

- Make the purpose of the DevOps teams very clear
- DevOps were expected to have scripting skills, then Developing skills, we 
  have now moved beyond that to where DevOps requires "people" and "process"
  skills
- Promote knowledge sharing
  - Through chat, e-mail weekly, monthly/weekly sharing video sessions
  - Feedback loops: many teams would be using your infrastructure, tools and
    automation so it is important to have a proper feedback channel in-place
- Use of internal platforms tailormade to the organization are correlated with
  high devops adoption
    - Those platforms need to be managed as an isolated project
- Promote autonomy and remove blockers due to approvals or lack of trust (take risks)
  - Create automation and guardrails to reduce burden instead of creating barriers
  - "Our purpose is not to create roadblocks and say no, it is to figure out how
    to unblock them and get to the 'yes'"
- Buy-in from leadership is paramound
- make as much as possible self-service
- dont focus on automation to the detriment of team interaction and
  collaboration
- Certifications are important for contractors, not so much for internal employees
- never label blockers as "cultural", because people think culture is
  "immutable" or hard to change
- Build proofs of concept, you don't want to have developers reach out for
  something you don't have in place or don't know how to do, build it, test it,
  learn it
- Collaboration can be expensive, so try to have the right type of collaboration
- Don't assume anything

> tags: devops; sre; survey;

> uid: 20210728133231Z

> links: 

