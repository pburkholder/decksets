

^Hi. I'm Peter Burkholder, with cloud.gov, I spend most of my days 
working with federal agencies to adopt cloud.gov, and more generally, the
notion of working in a PaaS or other high-level computing abstraction.

^So it's a relief to be with folks who understand something about Cloud 
Foundry, and about working with technology in government, and the joys
and challenges of that work.

^To understand the mission of cloud.gov, and it's raison d'etre, I think
it's worth reflecting on whytech in government is challenging.

---

^Before I started with the federal government 2 years, I would assume
the worst about the folks behind a government website or other IT system
that I was obliged to use, or would read about in the headlines. Thanks to 
Mark Schwartz, I started to better understand the good intentions behind the
bad outcomes.

^We know that the best outcomes in technology are built on teams with a high-level 
of psychological trust, and when teams are empowered to deliver value without outside 
impediment. Trust is the key ingredient. But trust can become a rare commodity: our 
constitutional system is predicated on the populace not trusting the government, on the
three branches set up to provide checks on the others' powers. Contracting and procurement
are set up to not trust the person making the procurement (for fear of favoritism or 
nepotism), let alone the bidders on a contract. 

---

All of this feeds into what Brad Katsuyama of IEX has identified as the regulated industry
death spiral: A loophole or oversight exists, it's exploited, resulting in scandal. The
response is to write more regulation. This bleeds talent, bleeds innovation, bleeds resources.
So we're now more likely to miss a loophole, and the spiral continues.


The regulatory spiral Specific to our domain is the ATO process. Any US Government information system, like a web application, must be granted an Authority to Operate, or ATO. Pertinent to CIO signing off on the ATO, and going to production, there are 4006 pages of regulations 4006! As a result, just the ATO process can take 6-14 months. 

To inject innovation into the cycle, the last administration established the Presidential Innovation Fellow program in 2012, which lead in 2014 to the creation of 18F: a digital consultancy within the federal government, housed within the General Services Administration. 
The team assembled there tackled problems by starting from user-centered design, agile development, lean acquisition and open-source practices. 

But thanks to those 4006 pages of regulation standing between their work and obtaining an ATO, their work was either stranded, or stuck. 

The shortcut to an ATO is to start with most of those 4006 pages of regulations already satisfied by re-use of technology -- and cloud computing is a huge boon here. The Federal government recognized that with FedRAMP program, where cloud service providers could get authorization that they met a certain number of compliance "controls", and tenants could build on top of their infrastructure or service and largely inherit those controls. 

The problem in 2015 was that the FedRAMP Marketplace didn't have a authorized general-purpose PaaS. If you started with IaaS provider, you could inherit controls for, say, the Physical Environment, Media Handling and Network Controls, but you were still responsible for all the operating systems, programming languages, logging, patching, etc. etc. So if you had 325 controls to satisfy for your application that had a Moderate risk profile, maybe you could re-use 85 of those, and then take on the work of satisfying the other 240. Ouch.

The 18F answer was to build their own PaaS, satisfy as many of those controls as possible, and make that available as Platform-as-a-Service for other agencies throughout government. The cloud.gov platform was launched as a platform for federal users on 9 Oct 2015. And if you we're present at the 2015 or 2016 CF summits, you may have caught Diego or Bret talking about cloud.gov.

<!-- https://18f.gsa.gov/2015/10/09/cloud-gov-launch/ -->

<!-- https://schd.ws/hosted_files/cfsummit2016/13/CFSummit2016-cloud.gov-compliance.pdf -->
<!-- 2m 20s -->

---

Fortunately there   