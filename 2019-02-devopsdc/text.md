build-lists: true
slidenumbers: true


# 🌱Culture is not Squushy🌱

## Peter Burkholder

## DevOpsDC, February 2019


^A few weeks ago at work there was some discussion whether our group had the same values and drive as we did a few year ago, and I jumped in with what I thought was an obvious answer, namely:

^T.C. Baxter in the key bowl

---

# "Let's measure our Westrum typology!"

^Suggested to mgmt that we do Westrum surveys', much like "Lets do coffee!" -- assuming a) universal knowledge and b) universal agreement. 

^There comes a time when you work with smart, closely aligned colleagues when you're surprised when they don't  know a thing that you think is obvious and of clear value. And knowing that they're smart and competent, maybe you should question your assumptions and value proposition.

^So let's tackle some of the assumptions that I was making, starting with some DevOps history. Back in 2009, Patrick Debois organized the first Agile Infrastructure conference, and to harness Twitter's 140-character limit, he dubbed it DevOps Days, a term that we carry with us still. Since there's no DevOps Manifesto, DevOps has been defined variously be diff practitioners, but an early outline came from John Willis and Damon Edwards, namely:

---

# CA(L)MS (2010)

* Culture
* Automation
* (Lean)
* Metrics
* Sharing

^ and at that time John said nothing more about it other than: "People and process first.  If you don’t have culture, all automation attempts will be fruitless." Which may be true but isn't particularly helpful.


^ And for the next few years, I think culture in DevOps was squushy by people who applied a "you know it when you see it" mentality, but measuring it came more into focus as some rigor started to be applied to our DevOps attributes. A good example of this squushiness is provided by the first "State of DevOps reports"

---

# Puppet state of DevOps reports

* Key Players:
  * Gene Kim
  * Jez Humble
  * James Turnbull
  * John Willis
* 2012 Survey Data
* Report to Velocity, June 2013

---

## High Performing DevOps Teams (2012)

* They’re more agile
  * 30x more frequent deployments
 * 8,000x shorter lead time (minutes/hours vs. months/quarters)
* They’re more reliable
  * 2x the change success rate
 * 12x faster MTTR


[.footer: https://www.slideshare.net/realgenekim/2013-velocity-devops-metrics-its-not-just-for-webops-any-more]
[.theme: Courier,1]

--- 

## Measuring Culture (2012)

> “I’ll tell you EXACTLY what devops means. Devops means giving a shit about your job enough to not pass the buck. Devops means giving a shit about your job enough to want to learn all the parts and not just your little world. Developers need to understand infrastructure. Operations people need to understand code. People need to fucking work with each other and not just occupy space next to each other.” 
-- John Vincent | @lusis | http://bit.ly/12DkRhf

[.footer: https://www.slideshare.net/realgenekim/2013-velocity-devops-metrics-its-not-just-for-webops-any-more]

---

##  Measuring Culture (2012)

* Trust (and Verify)
* Continuous Improvement vs Risk Management Theater
* “Human Error”
* Heroes / "high performers

[.footer: https://www.slideshare.net/realgenekim/2013-velocity-devops-metrics-its-not-just-for-webops-any-more]

^ They identified that they need to measure culture, to identify High Mgmt Trust vs Low Mgmt Trust styles, and that they needed metrics that enable regression, using a "Likert-type scale"


^ until Nicole Forsgren starting working with Puppet on the State of DevOps Survey in 2013, and published their first report in 2014.

---

On my team...

* information is actively sought.
* failures are learning opportunities, and messengers of them are not punished.
* responsibilities are shared.
* cross-functional collaboration is encouraged and rewarded.
* failure causes enquiry.
* new ideas are welcomed.

^The 2013 survey introduced questions, which you were to rank on a scale from 1 to 7, with 1 being Strongly diagree and 7 being strongly agree

^These questions did not come out of vacuum. Indeed, they're directly from this 2004, paper:

---

![fit](media/westrum2004.png)

[.footer: Westrum R A typology of organisational cultures BMJ Quality & Safety 2004;13:ii22-ii27.]

^You'll note, if you're sharp-eyed, that the journal is about business, or technology, but from the BMJ Quality & Safety. What does quality and safety have to do with DevOps?

^Jesse Robbins at AWS was a firefighter. John Allspaw of 10 + Deploys a Day at Flickr was pursuing a degree in  Human Factors and Systems Safety at Lund University. Sydney Dekker's work in avaition system was getting attention, as from this tweet:

---

![fit](media/dekkertweet.png)

^So when you're casting about for way to quantify DevOps culture, safety culture is good place to start. But it turns out there a lot of ways to measure how a workplace environment. First


---

# Organizational Culture 

# vs.

# Safety Culture

^Org culture like to talk about comp factors model, external & differentiation/internal & intergration vw stability + control & flexibility and freedom.  Clan/Market, Hierarchy/Adhocracy, from Quinn and Cameron, 1980s.

---

# Safety Culture 

# vs.

# Safety Climate

---

# A sampling of safety culture measures:

* White & Wilson: 113 questions on a 7-point scale
* Competing Values Framework: 65 questions, 1-5 ranking
* Team Climate Inventory: 44 items across 15 subscales
* Ostroff Organizational Climate Survey: 94 Items
* Zohar 2005: Only 16 questions, but
  * Considers safety when setting production schedule
  * Quickly corrects any safety hazard

---

# Ron Westrum, Eastern Michigan University



**Pathological organisations** are characterized by large amounts of fear and threat. People often hoard information or withhold it for political reasons, or distort it to make themselves look better.

**Bureaucratic organisations** protect departments. Those in the department want to maintain their “turf,” insist on their own rules, and generally do things by the book — their book.

**Generative organisations** focus on the mission. How do we accomplish our goal? Everything is subordinated to good performance, to doing what we are supposed to do.

[.autoscale: true]
The Study of Information Flow: A Personal Journey; Westrum

---

Pathological  | Bureaucratic | Generative
-------|--------- | ----------
_Power-oriented_ | _Rule-oriented_ | _Performance-oriented_
Low co-operation | Modest co-operation | High co-operation
Messengers "shot" | Messengers neglected | Messengers trained
Responsibilities shirked | Narrow responsibilities | Risks are shared
Bridging discouraged | Bridging tolerated | Bridging encouraged
Failure leads to scapegoating | Failure leads to justice |Failure leads to inquiry
Novelty crushed |Novelty leads to problems | Novelty implemented

---

# Information Flow

* _*Suppression*_: Harming or stopping the person bringing anomaly to light
* _*Encapsulation*_: Isolating the messenger, so the message is not heard
* _*Public relations*_: Putting the message "in context" to minimize impact
* _*Local fix*_: Responding to present case, but ignoring possibility of others
* _*Global fix*_: An attempt to respond to the problem wherever it exists 
* _*Inquiry*_: Attempting to get at the "root causes" of the problem

[.autoscale: true]

^ How do you measure culture. In his typology paper, Westrum lamented there wasn't a good tool for this:

---

> The true need is for a scheme that captures one or few dimensions in an easy to understand way
--- Ron Westrum

---

# Likert scales

* Do you feel you can provide feedback to management and it will be genuinely taken into consideration?
* I can provide feedback to management and it will be genuinely taken into consideration.
  * 1 <-- Strongly disagree .... 4 .... Strongly agree --> 7

[.build-lists: true]

---

# [fit] Results

---

![inline](westrum_inputs.png)

^ Lean mgmt from ADO is Team experimentation, working in small batches, gathering and implementing customer feedback

---


![inline](westrum_outputs.png)

---

> Westrum organizational culture is highly correlated with (eNPS)27 and that elite performers are 1.8 times more likely to recommend their team as a great place to work.

> In 2016, 31% of respondents were classified as pathological, 48% bureaucratic, and 21% generative.

Excerpt From: Nicole Forsgren, PhD, Jez Humble and Gene Kim. “Accelerate.” iBooks. 

---

# Let's measure this! What could possibly go wrong?

---

# Measure:

* How would you measure?
* Who else is doing this?
* What could you learn?

---


# Cinderella

^ "Does the isolated generative unit become a Cinderella, the target of hostile jibes and political actions?"

---

# Does culture matter?

# Can you measure it?

# Can you change it?

---

---

# Trust

* Psychological Safety
* Team Empowerment
* Regulatory Setting

---

# References

https://www.devopsdays.org/blog/2009/11/11/devopsdays-2009-belgium-a-great-success/

First Westrum DevOps Survey https://www.researchgate.net/publication/263198947_2014_State_of_DevOps_Report

John Willis: http://itrevolution.com/devops-culture-part-1/ - A Dive into Devops Culture

2013 State of DevOps Slides (June): https://www.slideshare.net/realgenekim/2013-velocity-devops-metrics-its-not-just-for-webops-any-more



John Willis: https://blog.chef.io/2010/07/16/what-devops-means-to-me/ - 2010 first blog post on CAMS, following 2010 Mountainview DevOpsDays


Schulte, Mathis & Ostroff, Cheri & Shmulyian, Svetlana & Kinicki, Angelo. (2009). Organizational Climate Configurations: Relationships to Collective Attitudes, Customer Satisfaction, and Financial Performance. The Journal of applied psychology. 94. 618-34. 10.1037/a0014365. 

Zohar, Dov, and Gil Luria. "A multilevel model of safety climate: cross-level relationships between organization and group-level climates." Journal of applied psychology 90.4 (2005): 616.

---

```sh
mmdc -i westrum_inputs.mmd -o westrum_inputs.png -b transparent
mmdc -i westrum_outputs.mmd -o westrum_outputs.png -b transparent
```