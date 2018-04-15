footer: @clouddotgov

# `#hi`

^Hi. I'm Peter Burkholder, with cloud.gov, I spend most of my days working with federal agencies to adopt cloud.gov, and more generally, the notion of working in a PaaS or other high-level computing abstraction.

^So it's a relief to be with folks who understand something about Cloud Foundry, and about working with technology in government, and the joys and challenges of that work.

^To understand the mission of cloud.gov, and it's raison d'etre, I think it's worth reflecting on whytech in government is challenging.

---

# Trust

^Before I started with the federal government 2 years, I would assume the worst about the folks behind a government website or other IT system that I was obliged to use, or would read about in the headlines. Thanks to Mark Schwartz, I started to better understand the good intentions behind the bad outcomes.

^We know that the best outcomes in technology are built on teams with a high-level of psychological trust, and when teams are empowered to deliver value without outside impediment. Trust is the key ingredient. But trust can become a rare commodity: our constitutional system is predicated on the populace not trusting the government, on the three branches set up to provide checks on the others' powers. Contracting and procurement are set up to not trust the person making the procurement (for fear of favoritism or nepotism), let alone the bidders on a contract. 

---

# Death spiral

^All of this feeds into what Brad Katsuyama of IEX has identified as the regulated industry death spiral: A loophole or oversight exists, it's exploited, resulting in scandal. The response is to write more regulation. This bleeds talent, bleeds innovation, bleeds resources. So we're now more likely to miss a loophole, and the spiral continues.

^The regulatory spiral Specific to our domain is the ATO process. Any US Government information system, like a web application, must be granted an Authority to Operate, or ATO. Pertinent to CIO signing off on the ATO, and going to production, there are 4006 pages of regulations 4006! As a result, just the ATO process can take 6-14 months. 

^To inject innovation into the cycle, the last administration established the Presidential Innovation Fellow program in 2012, which lead in 2014 to the creation of 18F: a digital consultancy within the federal government, housed within the General Services Administration. The team assembled there tackled problems by starting from user-centered design, agile development, lean acquisition and open-source practices. 

^But thanks to those 4006 pages of regulation standing between their work and obtaining an ATO, their work was either stranded, or stuck. 

^The shortcut to an ATO is to start with most of those 4006 pages of regulations already satisfied by re-use of technology -- and cloud computing is a huge boon here. The Federal government recognized that with FedRAMP program, where cloud service providers could get authorization that they met a certain number of compliance "controls", and tenants could build on top of their infrastructure or service and largely inherit those controls. 

---

# Aral Sea

^The problem in 2015 was that the FedRAMP Marketplace didn't have a authorized general-purpose PaaS. If you started with IaaS provider, you could inherit controls for, say, the Physical Environment, Media Handling and Network Controls, but you were still responsible for all the operating systems, programming languages, logging, patching, etc. etc. So if you had 325 controls to satisfy for your application that had a Moderate risk profile, maybe you could re-use 85 of those, and then take on the work of satisfying the other 240. Ouch.

^The 18F answer was to build their own PaaS, satisfy as many of those controls as possible, and make that available as Platform-as-a-Service for other agencies throughout government. The cloud.gov platform was launched for federal users on 9 Oct 2015. And if you we're present at the 2015 or 2016 CF summits, you may have caught Diego or Bret talking about cloud.gov. It's been awhile, and a lot is new.

<!-- https://18f.gsa.gov/2015/10/09/cloud-gov-launch/ -->
<!-- https://schd.ws/hosted_files/cfsummit2016/13/CFSummit2016-cloud.gov-compliance.pdf -->

---

# Compliance and Security

^So let's do whirlwind tour of what cloud.gov offers, because those feature may be relevant to your use case.  We, of course, offer the core functionality of Cloud Foundry: the ability to run application code for you in the cloud, along with self-service managed marketplace offerings. From a government perspective, our killer feature is security and compliance.

^First, we're FedRAMP authorized for workloads up to FISMA moderate.  (More TKTK)

^Second, because we're platform-as-a-service, instead of infrastructure-as-a-service, a tenant can inherit a far larger number of security and compliance controls. For example, if you're running a FISMA-moderate workload, your security plan for an ATO needs to address 325 of NIST 800-53 controls. If you're building atop a typical IaaS, you can inherit and reuse TKTK controls from the cloud service provider, like assurance there's fire suppression in the datacenter.  When you run atop cloud.gov, you can inherit and reuse up to TKTK of those controls, document how we share responsibility for TKTK, and then you're fully responsible for the remaining TKTK.

^Third, we enable tenant security by making the secure choice the default choice. By reducing cognitive burden at the platform level, product teams can focus on security in their source code. Examples: S3 buckets are either public or private, and that's that, reducing the chance stashing private data in a bucket that is later accidentally exposed. S3 buckets enforce server-side encryption. DBs are encrypted at rest, and only allow TLS connections. The platform is continually updated, and we.


^Lastly, we're because we're a built-for-compliance offering, we're always looking for ways to make compliance easier on tenants. We notify our users when their buildpacks are out-of-date.  We're the only FedRAMP CSP to have an active bug bounty program. As Bret will tell you later, we're extending our container security with SysDig Falco.
<!-- I've only check AWS, Azure and CSP on this. -->

---

# News you can use

^Beyond these core security and compliance features, we've enhanced or extended Cloud Foundry offering, and I'll highlight a few of those in case you want to use them in your work, as we open-source everything we can:

---

| Customer facing: | |
| --- | --- |
| cloud.gov Dashboard (like Stratos)  | Kibana proxy for tenant logs |
| CDN Broker for CloudFront + LetsEncrypt | Identity Broker to reuse UAA for applications |
| Notify tenants on outdated buildpacks | Sandbox-bot: sweep clean after 90 days |
| RDS & S3 Brokers | Redis & Elasticsearch Brokers for K8S |

---

| Infrastructure: |
| --- |
| Bosh: Ship CF audit logs to CloudWatch |
| Bosh: Create free Sandbox accounts |
| Bosh PowerDNS for DNSSEC support |
| Bosh releases for: ClamAV, Nessus, NewRelic, Tripwire, Snort, Ubuntu hardening|
| NGINX proxy for CF Router to force HTTPS, add HTTP headers, set timeout & size limits |
| All the Terraform plans and Concourse pipelines to build cloud.gov |
| BugBounty: Not a service, but we can provide advice | 

---

| Plugins: |  |  |
|--- | --- | --- |
|service-connect | migrate-db | route-lookup |

--- 

# Making a difference

^ The folks at 18F originally adopted Cloud Foundry to solve their delivery problem, they made into _cloud.gov_ to change how agencies operate. How has that worked out?

---

Agencies: | <br> | <br>
---|---|---
NOAA | Air Force | GSA
FDIC | FEC | Forest Service
Interior | Education | IRS
FBI | EPA | OMB
NSF |  USDS | ATF

---

## Federal Election Commission

## Forest Service e-Permitting

## Federal Deposit Insurance Corporation

---

## Federalist 

--- 

<!-- 
# Globally
* United Kingdom GDS
* Australia 

N.B: Not doing this slide. Too hard to get right, doesn't add enough value.
-->

---

The road ahead| <br> 
---|---|
Multiple Clouds: |  Windows
CI/CD-as-a-Service | Container Runtime 
Isolation segments / TIC | FedRAMP High

## Adoption, adoption, adoption

---

# Clearing the five barriers to adoption

^In the order that we need to tackle them....

^I have partial answers here, but I know they're complete. So the exent that you can solve, or share your ideas, I'm eager to hear them.

---

## 0. :ear:?

^I'm not indexing from 0. In this case there's a preliminary hurdle in that I don't talk much to the people who haven't heard about cloud.gov. Our ability to market is pretty limited, so the extent to which you can tweet or write or talk about us, the better. Thanks you. So once we do talk to folks, the first hurdle is:

---

## 1. The ☁️ is someone else's 💻

^Although the sticker: "There is no cloud, it's just someone else's computer" is cute and has a point, it points to a persistent mental model of thinking about "computers" instead of "compute" or even more broadly, of outcomes or your mission.

^A typical example of this was a pricing conversation we had with a potential customer, who shared with us the quote from an IaaS contractor. The quote spelled out the specifications, in CPUs and GBs, not just for the AppServer itself, but also for the Varnish caching server, the NginX web server, the Redis server, and the DB Cluster itself. There was no mention of using IaaS provided database services, or scaling groups, or load balancers, let alone the cloud value add of a CICD pipeline.

^People can visualize their servers humming in racks in their datacenter, and perhaps they still have names. Moving to naive IaaS, or lift-and-shift, fits that model, but brings few if any benefits.

^The best I can do at this point is to talk the mission-enablement provided by the code that's bundled in, say, a J2EE WAR file. Then consider all the bit in an IaaS needed to run that WAR file: VPC, jumpbox, server, OS, Java install, J2EE runtime, scaling group, load balancers, SSL certs, etc. Not to mention what the deployment process is going to be. None of that provides value as such. Only what runs in the WAR. With cloud.gov, you provide the WAR, and the platform takes care of the rest.

^But clearing that mental model wall brings us crashing into:

---

## 2. The broken mirror

^The person you're talking to, when they look in the mirror, sees someone who has years if not decades of experience running datacenters, spec'ing out hardware, configuring firewalls and routers, and learning the ins & outs of various operating systems. What we propose is really threatening to their identity. We're not taking away their worries, we're potentially taking away their sense of self.

^This is real, and even if, or particularly if, some administrator mandates a move to a PaaS. And it's unlikely that the true motivation behind this resistance will be discussed openly.

^What I'm finding is that it works to shift the conversation to all the things the PaaS doesn't do. The PaaS won't run every application. The applications that aren't cloud-ready need their expertise to get them to cloud ready. The PaaS is still dumb: it doesn't know how to scale your application. It doesn't know what to do with the logs it ships you. That's still on you. And the PaaS doesn't do all the things you've been wanting to do but never had time for: real CI/CD, meaningful dashboards, sensible alerting so you can sleep through the night, or finally getting the developers the tools they need.

^The broken mirror has one particular manifestation that needs to be called out as its own barrier. Namely, that "we already have a PaaS"

---

## 3. PaaS ✅

^We alread

---

## 4. PaaS 🚫

---

## 5. 

# Thank you!

(Image of our team from Zoom)

---

### 

---

# References and Resources

Mark Schwartz, How DevOps Can Fix Federal Government IT, https://www.youtube.com/watch?v=QwHVlJtqhaI, DevOps Enterprise Summit 2014

Jen Pahlka, "Death Star Thinking and Government Refrom", Journal of Design and Science, https://jods.mitpress.mit.edu/pub/issue3-pahlka

Brad Katsuyama, Regulatory Death Spiral. _N.B._ I've been unable to find this other than one photo of slide online. Thanks to Julian Dunn for bringing it to my attention.





