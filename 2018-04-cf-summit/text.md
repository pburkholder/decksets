theme: next,1
footer: ![inline 8%](https://www.cloudfoundry.org/wp-content/uploads/2017/10/cloud-gov.png)
build-lists: true
slidenumbers: true

# Enabling Innovation in Government with Cloud Foundry
## Peter Burkholder

![inline](media/logo.png)

[.background-color: #FFFFFF]
[.header: #28517c]
[.hide-footer: true]


---

# `#hi`

^Hi. I'm Peter Burkholder, with cloud.gov, days working help federal agencies adopt cloud.gov, and explaining Platform-as-a-Service.

^s exciting understand Cloud Foundry, already  using it government or highly-regulated setting. 

^To understand cloud.gov and its mission, key ingredient to working : Trust

---

# Trust

* Psychological Safety
* Team Empowerment
* Regulatory Setting

^We research team productivity and DevOps practices best outcomes teams high-level of psychological trust, and when teams empowered, entrusted, deliver value concept to production.

^1! is internal to a team: your voice is heard, that you can fail without blame or shame. 2! is team context: Are trusted operate in domain expertise? failure treated learning opportunity and not punishment? 

^Latter trust tension with a 3! regulatory setting. And within government, trust rare by design: 


---

[.hide-footer: true]

![](https://gdb.voanews.com/F7B0DC49-51F8-4087-98FF-4CB88B380375_w1023_r1_s.jpg)

^our constitutional spredicated on the populace not trusting the government, on the three branches providing checks. 

^Procurement to not trust the people making the buy favoritism. Not trust the contractors .

^Replaced by regulation and audit; fine -- it enables a bureaucracy to operate on behalf 

<!-- ^Still, it can feed regulatory escalation: A loophole exists, it's exploited, resulting in scandal. The response is to write more regulation. And so on. -->

^Now, framework for tech government AUTHORITY..." process. Any US Government IS, like a web application, must Authority to Operate, or ATO. The ATO 200-1000 pages, address all these published 

---


![original](media/6600.png)

# <br>
## Total 
## pages: 
## ~6600

[.header: #EE0000, alignment(right)]


^So 3 years ago, 18F was in a QUANDARY. 18F is a housed within the GSA, and we PARTNER with other agencies PRINCIPLEs
including 

^USER-centered design, AGILE development, LEAN acquisition and OPEN-SOURCE practices. 

^So in conjunction with agency partners they were BUILDING great product. Yet the challenge of COMPLYING with and _DOCUMENTING_ compliance STRANDED, ....

---

![](https://farm4.staticflickr.com/3654/3417016257_6eb962033d_o_d.jpg)

[.footer: https://www.flickr.com/photos/martijnmunneke/3417016257]

^because they were looking at a process where typically...

---

![](https://farm4.staticflickr.com/3654/3417016257_6eb962033d_o_d.jpg)

[.footer: https://www.flickr.com/photos/martijnmunneke/3417016257]

### 6 to 14 months to ATO

^... it would take 6 to 14 months to obtain an ATO and actually ship. And that's when the cloud.gov began to coalesce.

---

![original](https://www.nasa.gov/sites/default/files/styles/full_width_feature/public/images/450093main_hobys_rosette_05_A3_3d_full.jpg)

# Genesis
[.header: #FFFFFF]

^One shortcut to ATO: Reuse! But in January 2015 the reuse of configuration management tooling wasn't SCALING to the needs of the 18F, ASSESSING the  tradeoffs between CLOUD & COMMERCIAL`, a small team at 18F BUILT PaaS w/ Cloud Foundry 

^TO meet COMPLY and DOC and their partners.

^It was such a success internally, that folks decided to make it available to any agency, and in October 2015,

---

![fit](media/2015.png)

^ cloud.gov was launched for federal users. And if you we're present at the 2015 or 2016 CF summits, you may have caught Diego or Bret talking about cloud.gov. This is how it looked back then, but its been awhile, and a lot is new.

---

![fit](media/2018.png)

^A new look clearly, but a lot more under the covers. And we'll get into that, but since I wasn't around in those early days, I'd like to share the lessons I learned on my journey to being a true believer not just in cloud.gov, but in the paramount necessity for a high-level PaaS in highly-regulated environments.

---

# From digging to DevOps

![inline](https://clubrunner.blob.core.windows.net/00000008680/Images/P-Chung.jpg) ![inline](https://secure.meetupstatic.com/photos/event/c/c/c/5/600_467212421.jpeg)

^I first as a geophysicist, field work and data analysis, and then sysadmin for LABS and the PRIVATE . I caught the DevOps bug in 2010, SOON AS HEARD, as it PULLED together AUTOMATION and testing, and with the FRAMEWORK for team collaboration.

^Before US Government, I'd spent two years with AUTOMATION VENDOR, where I'd spent time COACHING around DevOps, I struggled to NURTURE DevOps in REGULATED , though, and would see weird ANTIPATTERNS emerge when  TEAMS wouldn't TRUST each OTHER's use of the TOOL.

---

# 18F

![inline](https://18f.gsa.gov/assets/blog/join-us/18F-IRL-2016.jpg)

^ CRACKED, Started, Dismissive: Heroku - Not for REAL SysADMIN - DevOps Toolkit

^Agency First effort. Not coaching, In trenches, w/ partner. 

^Hardned, Functional, Repeatable, Automated.  NINE months, no Developer code.

^"had exceeded all expectations" by having a repeatable process for building and managing that environment. 

^real step forward for them,  my colleagues at 18F SHIPPING and RELEASING with their partner agenices using cloud.gov. I joined  with TWO Lesson Crystalizing.

---

# 1: A PaaS is a prerequisite for DevOps outcomes in regulated environments

^Want DEVOPS. Read HiPerf Speed & Stability. But -> Tooling and Forms, Not OUTCOMES

^Core DevOps: Empower Deliver Value/Mission. No BottleNeck

^StartUps/Mature : EMBED ops TEAM, GRANt AUTHORITY to make changes on behalf on the organization.

^Yes: you can run terraform to build a new test env. Yes: you can run that Chef recipe to install Tomcat.

^government and regulated industries are low-trust organizations. Even with Infrastructure-as-Code -- they trusted to write code handling credit card data, they wouldn't trust to write code to install Tomcat on their systems.

<!--When I worked for Chef Software, I would see organizations with multiple Chef runs: One for ops and security, and one for the developers. 
-->

^BEGGING: please APP SERVER AND DB SERVER IN A SHARED ENV, and has the ops teams wORKING HARD as ever.

^A PaaS is a prerequisite for DevOps outcomes in government. 

---

# 2: Absent a real PaaS, organizations will attempt their own

^You have these mature automation tools, you want guardrails for product and dev teams, it's tempting to build a toolchain bespoke to the organization's needs.

^drive of "let's build our own PaaS" takes hold. 

^This might take the form of something like: "I know, let's kick of the process with a Remedy ticket, which opens up a Puppet/Chef/Terraform template they can fill in, and commit to Git. The PR gets routed to Pat or Steve for approval, then it'll get instantiated in a validation environment for security scans ... " and so and so on. 

^Toolchains are AWESOME, but NOT at SCALE when NO FLOW. SEEN this DEVOLVE into Platform-as-a-Concierge-Service (or PaaCS), with BOTTLENECKS  Manual work.

^STOP THIS. EASU use PaaS for the 80% use case, and let OPS do HARD WROK. I get to. What is this cloud.gov thing?

---

# What is cloud.gov?

* Cloud Foundry, 100%<sup>*</sup> open-source
* Standard buildpacks, brokers for RDS, S3, ES, Redis, etc.
* Running atop AWS GovCloud
* Only for US government
* Security by convention
* With a dollop of compliance:


^Anyone from the US Gov can work in a free sandbox. But we're only for USGov use at this point; expanding to states and localities isn't in the picture at this point. 

^secure choice the default choice. Focus on source code and functionality. Example: S3 buckets... 

^From a government perspective, our killer feature is security and compliance, first among this is FedRAMP authorization.

---

# Compliance

FedRAMP JAB P-ATO, FISMA Moderate, January 2017.

^Let's unpack that:

---

# Let's unpack that

* FedRAMP
* JAB
* P-ATO
* FISMA Moderate
* January 2017

[.build-lists: true]

^August 2016: Began our review with the JAB teams. 23 weeks from JAB kickoff to signed P-ATO, including 8 weeks for technical/operational improvements and 15 weeks for JAB review. 470 pp, fortnightly meetings, monthly conmons, annual reassessment.


^What this gets us for our tenants is a sign lift of their compliance load.


---

![](media/325-graph.png)

[.hide-footer: true]

^As mentioned, if you're running a FISMA-moderate workload, your security plan needs to address 325 controls and if you're building atop a typical IaaS, you could inherit and reuse ~100 controls. Physical env, physical security, media protection, perimeter security, maintenance. About 225 is on you. 

^When you run atop cloud.gov, you can inherit and reuse up to 269 of those controls, and then you have 56 which are shared or fully your responsibility. And I note we've leveraged FedRAMP ourselves by building atop AWS GovCloud, and inheriting of their 54 controls in our own SSP.

^These numbers are highly idealized!

---

# FedRAMP: What we learned

* Reflection
* Discipline
* Empathy
* Communication

^ Definitely good for our customers.
^ Reflected on what we offered, and yanked some features....
^ Discipline we would want to have regardless. We do quarterly reviews of our plans and processes, and are continually improving. 
^We better understand the our customers regulation efforts.
^ We got better at explaining what cloud.gov does, and how it works, and the value of open source.  

---

# Open source <br>all-the-things

![](media/repositories.png)

<!--[.header: #FF0000]-->

^All our work is open source, it means this it's out there for you to use.  There's a lot of it - the background image lists a bunch of them. I'll highlight a few that are essential or useful.

---

# Dashboard

![inline](media/dashboard.png)

^Orgs, spaces, user invites, the broker marketplace, managing env var, stop/start and scale application, and other features.

^Mostly focussing on the non day-to-day non technial users.

^Australia contributions, Stratos likely will replace.

---

# UAA-authenticated Kibana plugin

![inline](media/kibana.png)

^We store customer logs with ELK for 180 days, but stored logs aren't much use if you can't view them. So any cloud.gov use can authenticate against UAA and see their logs, and their logs only, in Kibana. 

^Adam Kendall on our team wrote a UAA plugin for Kibana, so once authenticated all user searches are filtered to include the @cf_org_id and @cf_space_id. Not just useful, but another step forward in making it easier to operate in compliance

---

# UAA identity provider broker

![inline](media/identity.png)

^Since ALREADY using our CUSTOMER's agencies SINGLE-SIGN-ON with UAA, make it easier on to enable AGENCY AUTHENTICATION in their apps by just REUSING?

^The cloud.gov IDENTITY PROVIDER service has a SINGLE OAUTH-CLIENT plan, and you PROVIDE rEDIRECT URI AND SCOPE. The APPcan then get the CREDENTIALS to your PROVIDER with SERVICE KEY

^I've shown one example, I BUY, get REDIR

---

# Behind the scenes

* Lots of BOSH Releases
* Terraform plans and Concourse pipelines
* Bug Bounty

^ 1, 2, 3

^Set aside money for bounties, paid very little, did get notified on a few things to tighten up, mostly feedback that they were impressed by our work.

^So 18F made _cloud.gov_ to change how agencies operate. How has that worked out? Here are our most active partner agencies, 

--- 

# Making a difference

Agencies: | <br> | <br>
---|---|---
NOAA | Air Force | Forest Service
FDIC | Education | IRS
FBI | EPA | OMB
NSF | USDS | ATF
**FEC** | **Interior** | **GSA**

(plus 71 agencies in sandbox orgs)

^ spanning broadly across government. NOAA, AirForce... 

^One good case study is the Fed Elec Commission. 

---

![right fit](media/fec.png)

# Federal Election Commission

> **We had a complete culture change about how to do user-centered design and agile.**
-- FEC product owner

^cost savings, ELASTIC. it matters that they save 85% on operation. Key TRANSFORM. QUOTE:

^Agile from inception to delivery. Instead of quarterly releases, they now deliver bi-weekly, and are engaged in user-centered design and rapid prototyping. 

^COST-savings, and better CAPACITY, and  DELIVERY on their mission. Dept of eDUCATION and College Scorecard; the FDIC; The FOREST sERVICE; 

^And sometimes it's the little things that matter, like our fourth graders:

---

![](media/ekip.png)

^Who can now get free passes for our federal lands and waters Thanks to the Every Kid in a Park Program. 

^This site was tied to a scheduled presidential announcement date, and it turns out that those dates are fixed once they're set. With a 90-day deadline on the line, 18F partnered with Interior to design, build and launch it in time for the announcement. 

^And it turns out the static sites have been an overlooked need for federal offices.

---

![original](https://raw.githubusercontent.com/18F/federalist-docs/master/assets/images/how-federalist-works-for-presentation.png)

[.hide-footer]

^Many offices just need a static website they can update as needed. CMS's
are overkill for them, so our sibling project Federalist lets people edit locally, push to GitHub, preview on the web, and then publish.

^Federalist now hosts 119 sites for eight federal agencies, and updates are happening hundreds of time per week.

^More generally Within GSA, many of our products are now built for cloud.gov, and we have team adept at generating the require documentation, and at working with our auditors.   Remember 6-14 months to ATO?

---

![original](https://farm2.staticflickr.com/1023/784286985_51338a3fe1_o_d.jpg)

# <br>
# <br>
# <br>
# <br>
# <br>
# <br>
# 1 month to ATO

[.header: alignment(right)]

^As the auditors are also now familiar with cloud.gov, this ATO Sprinting Team can now obtain ATOs in about a month.

^All this has us looking forward to 

[.footer: https://www.flickr.com/photos/robwallace/784286985]

---

The road ahead: | <br> 
---|---
FedRAMP High | Windows
CI/CD-as-a-Service | Container Runtime 
**Vendor Adoption** | **Multiple Clouds**

^All these things matter: 1,2,3,4

^As a government customer, you may be interested in a product that, as SaaS, is going to be hard buy because its not FedRAMP'd. ON the flip side, it may be time consuming and expensive to run "in-house". If the vendor certifies it runs in cloud.gov, then the gov customer can access better product in less time in their acquisition. Same compliance profile, smaller operational footprint

^And as Abby mentioned, many enterprises are running cloud foundry across multiple clouds. We aim to do the same for any Infrastructure that has a mature CPI support, and an appropriate authorization. This would yield huge benefits in Contingency Planning, allow workloads to run close to underlying services, and use the underlying provider with the best cost and feature offerings. Good for government, and good for competition. We expect to pilot that with Azure and Google Cloud this year.

---

# _cloud-gov-inquiries@gsa.gov_

![inline](media/logo.png)

[.background-color: #FFFFFF]
[.header: #28517c]
[.hide-footer]
[.slidenumbers: false]

^Technical excellence in highly regulated industries, and government, has challenges
around trust, which makes systems that enable higher-trust real enablers.

^We' demonstrated that with cloud.gov, and by moving forward with cloud.gova as a computer resource layer between government teams and underlying cloud providers, we can provide velocity and compliance and stewardship of tax dollars without vendor lock in.

---

 <br>
 <br>
<br>
# Thank you!

![original](media/cgteam.png)

[.header: #EE0000;, alignment(center), line-height(0), text-scale(1.0)]

---

# _cloud-gov-inquiries@gsa.gov_

![inline](media/logo.png)

[.background-color: #FFFFFF]
[.header: #28517c]
[.hide-footer]
[.slidenumbers: false]

---

# References and Resources 1/2 

Mark Schwartz, How DevOps Can Fix Federal Government IT, https://www.youtube.com/watch?v=QwHVlJtqhaI, DevOps Enterprise Summit 2014

Jen Pahlka, "Death Star Thinking and Government Reform", Journal of Design and Science, https://jods.mitpress.mit.edu/pub/issue3-pahlka

cloud.gov repositories: https://cloud.gov/docs/ops/repos/

Characteristics of a PaaS: https://csrc.nist.gov/publications/detail/sp/800-145/final

[.autoscale: true]

---

# References and Resources 2/2


Announcement of cloud.gov launch: https://18f.gsa.gov/2015/10/09/cloud-gov-launch/ 

Prior CF summit talks: https://schd.ws/hosted_files/cfsummit2016/13/CFSummit2016-cloud.gov-compliance.pdf

Kibana Auth: https://github.com/cloudfoundry-community/logsearch-for-cloudfoundry/tree/develop/src/kibana-cf_authentication and https://github.com/cloudfoundry-community/logsearch-for-cloudfoundry/blob/develop/docs/features.md#kibana-authentication-plugin

[.autoscale: true]
