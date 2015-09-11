---
title: 'Cloud Innovators: Netflix Strategy Reflects Google Philosophy'
link: http://cloudscaling.com/blog/cloud-computing/cloud-innovators-netflix-strategy-reflects-google-philosophy/
author: randybias
description: 
post_id: 1539
created: 2010/11/23 08:00:22
created_gmt: 2010/11/23 16:00:22
comment_status: open
post_name: cloud-innovators-netflix-strategy-reflects-google-philosophy
status: publish
post_type: post
layout: post
category: cloud-computing
---

# Cloud Innovators: Netflix Strategy Reflects Google Philosophy

Welcome to a new interview series we’re trying on at Cloudscaling. This series is meant to highlight not just cloud adoption stories, but stories about how businesses, particularly enterprise businesses, are changing the way they provide Information Technology (IT). As long time followers of the Cloudscaling blog know, our view is that “cloud computing” is neither [outsourcing](/blog/cloud-computing/the-cloud-is-not-outsourcing) (2009) or [virtualization-on-demand](http://cloudscaling.com/blog/technology/virtualization-is-not-the-answer-for-clouds) (2008), but something far more subtle and far-reaching: a [20-year shift in the way that all IT is provided](http://cloudscaling.com/blog/cloud-computing/elasticity-is-not-cloud-computing-just-ask-google), much like the transition from mainframe computing to enterprise computing (aka ‘client-server computing’). Just like when we transitioned from mainframes, a *lot* of change is going to happen. In order to highlight this change, we wanted to start a series that really shows what is possible if you fully embrace cloud computing. Our first interview is with [Adrian Cockcroft](http://perfcap.blogspot.com), Cloud Architect at Netflix. Recently Netflix announced something incredible: their 24x7x365 video-on-demand streaming service, the largest of its kind in the world, had moved from their own datacenters onto Amazon Web Services EC2. See this [QCon presentation](http://www.slideshare.net/adrianco/netflix-on-cloud-combined-slides-for-dev-and-ops) from Adrian on the technical details. This interview, however, takes a different tack and looks at why Netflix chose to take this route, examining business drivers, and asking “what do you tell others who wish to follow in your footsteps?” **The Interview** **RLB:** _Could you describe at a high level what Netflix is doing on AWS?_ **AC:** Encoding movies for streaming, log analysis, production web site and API, most everything that scales with customers and streaming usage. Easier to say what we don’t have there: most internal IT that scales with employee count, legacy stuff, DVD shipping systems, account sign-up and billing systems. We use Akamai, Limelight and Level3 CDN’s for streaming the movies, which is a cloud based service. There is an AWS CDN service, but they aren’t a big enough player in this space at this point. **RLB:** _What was the key business driver that led to deciding to use AWS rather than your own datacenters?_ **AC:** Business agility and the inability to predict how much capacity we would need when and where for a business whose growth is accelerating. Year on year customer growth is 52% (up from 42% last quarter), year on year customers using streaming is up 145% (from ~4M to ~11M). We need to be a small-ish fish in a big AWS pond to leverage AWS investment in datacenter build-out, rather than building our own pond. **RLB:** _Many folks claim that they can deliver a private cloud at a similar price point to AWS. I assume you ran the numbers yourself. In whatever detail you can share, what does the ROI look like for Netflix?_ **AC:** Our datacenter runs Oracle on IBM hardware, we could have switched to commodity hardware in a datacenter, but skipped that step by going to AWS. There are three points on cost, one is that Oracle on IBM is very expensive, so AWS looks cheap in comparison, and we have flat-lined our datacenter capacity. The second point is that AWS costs are fully burdened, and we could not have hired enough SAs and DBAs to build out our own datacenter this fast. We have added 4-5x as many systems in the cloud as the total we have in our datacenter over the last year. The third point is that the costs are elastic, you start paying for a resource just before it goes live, and if you stop using a resource you stop paying for it. If you own a resource it sits around a long time waiting to be delivered and installed, and if you no longer want to use that type of resource you are still paying for it for three years. When Amazon cuts prices, your installed capacity gets cheaper. When they install new instance types you can be running on them in hours, technology refresh in real time. I don’t believe private clouds can compete with public on price, however if you have a bunch of empty datacenter space or want to re-organize your internal systems to be automated and API driven then there are real cost savings to building your own private cloud. I think VMware and Microsoft are going to own the private cloud space, but Amazon is going to continue to disrupt both of them at a lower price point for public cloud. **RLB:** _You have a great presentation on SlideShare that describes your development and operations approach. You were willing to rethink your entire approach to the Netflix system. Why was your business leadership willing to take on this kind of risk/investment?_ **AC:** That’s the way they roll... The impetus to do this came from the top down. The leadership saw that the biggest technology risk we had was lack of agility, and wanted to invest in our ability to move faster than our competitors without being held back by scale (e.g. running out of datacenter capacity) or technical debt issues. The leadership had to drag the engineers along to some extent, wean them off SQL and established habits and processes. **RLB:** _Our belief is that 'cloud computing' is a new way of providing IT that displaces 'enterprise computing' as enterprise computing displaced 'mainframe computing'. Your work seems to epitomize this. What would you say to folks who are willing to re-architect/re-engineer their applications for this new world? What are the top 3 challenges they need to consider?_ **AC:** The key challenge is to get into the same mind-set as the Google’s of this world, the availability and robustness of your apps and services has to be designed into your software architecture, you have to assume that the hardware and underlying services are ephemeral, unreliable and may be broken or unavailable at any point, and that the other tenants in the multi-tenant public cloud will add random congestion and variance. In reality you always had this problem at scale, even with the most reliable hardware, so cloud ready architecture is about taking the patterns you have to use at large scale, and using them at a smaller scale to leverage the lowest cost infrastructure. The second challenge is mostly political, an enterprise CIO and IT/ops department would much rather build datacenters and private clouds than become irrelevant to their customers. However while they are struggling to get their private clouds to work, their end users will be using AWS and setting a fully burdened price point expectation that IT cannot get near to. I have heard of internal chargeback for resources being an order of magnitude higher than using AWS for the same kind of resources [1]. The third challenge is the obvious one that the organizations that run compliance audits are working to a rule-sheet that has no concept of cloud, and it will take a while for some applications and industries (like finance) to get permissions and processes in place. That’s a when not an if. **RLB:** _I've heard from folks who think they are in the know that enterprises aren't adopting AWS, yet Netflix, a mid-tier enterprise now has 'thousands' of servers running its most mission critical service on AWS. What do you say to these folks?_

## Comments

**[Gilad](#657 "2010-11-23 18:05:00"):** Great post! You inspired us to write up a post called "Cloud Computing sells itself", with some follow-on observations. We are seeing customers already bought into the public cloud idea, and asking the follow on questions (such as "how do I make it secure?"). Here: http://www.porticor.com/2010/11/cloud-computing-sells-itself-the-view-from-netflix/

**[Ray Nugent](#658 "2010-11-24 02:46:00"):** Randy, can you calculate the fully loaded cost of an hour of compute time in a private cloud? How does that compare to what public clouds cost? In other words is there a private cloud approximation of an EC2 instance hour?

**[randybias](#659 "2010-11-24 06:10:00"):** Good question, Ray. There is probably a ton of variance. We have some models that I could play with for public providers that might work. Will see what we can do. That would make for an interesting post.

**[securitycurve (SecurityCurve)](#661 "2010-11-24 13:40:00"):** Why did the #Netflix cross the cloud to Amazon AWS? Netflix Cloud Architect explains in an interview w/ [@Cloudscaling](http://twitter.com/Cloudscaling) http://bit.ly/bZ0ESU

**[leemcarthur (leemcarthur)](#663 "2010-11-24 15:53:53"):** Interesting interview with the lead architect on the NetFix move to AWS cloud for their primary offering: http://bit.ly/bZ0ESU

**[leemcarthur (leemcarthur)](#664 "2010-11-24 19:30:33"):** Interesting interview with the lead architect on the NetFlix move to AWS cloud for their primary offering: http://bit.ly/bZ0ESU

**[ccalipanvidea (Chris Cali)](#666 "2010-11-24 20:54:53"):** A convincing case for cloud computing applied to media. http://bit.ly/bZ0ESU

**[cues7a (Daniel de la Cuesta)](#668 "2010-11-25 10:10:41"):** More about Netflix migration to the cloud: http://tinyurl.com/27wsg26

**[gadmultimedia (GAD)](#669 "2010-11-25 10:10:41"):** More about Netflix migration to the cloud: http://tinyurl.com/27wsg26

**[appupatel (arpit)](#670 "2010-11-25 11:54:59"):** http://cloudscaling.com/blog/cloud-computing/cloud-innovators-netflix-strategy-reflects-google-philosophy #appdy

**[appupatel (arpit)](#671 "2010-11-25 11:56:22"):** http://cloudscaling.com/blog/cloud-computing/cloud-innovators-netflix-strategy-reflects-google-philosophy #appDynamics #cloud

**[Ops](#675 "2010-11-28 11:20:00"):** The moment I read this... "Our datacenter runs Oracle on IBM hardware, we could have switched to commodity hardware in a datacenter, but skipped that step by going to AWS", I stopped reading. Of course if you outsourced your technology strategy to vendors ( by using oracle rac, instead of thinking your data strategy , and buying the most expensive hardware out there without regards to costs, instead of mitigation of failure with software) then sure, anything will look cheap by comparison. Specially when you then throw OSS into the mix. I have yet to see, any company with any reasonable infrastructure ( which I'm assuming nextflix is one ), which does not reap huge cost savings by having things in house ( the caveat emptor being that it was to be well done). Maybe i'm too cynical, but all I gathered from his answers was; " I don't know how to run operations, so I fell for the dog and pony show". He's saying, I could have run things more efficient, but I didn't. Well, I guess he shouldn't be running operations then, someone else should be hired for that ;) Public Clouds are great for early stage when you don't know your scale. They are also great to leverage for large batch processing. But once you've reached the threshold of the first hundred server instances, their cost skyrockets beyond reason. Last two startups we've trounced public cloud pricing, all while maintaining scalability. But that does require competent staff and good negotiating skills :) Again, maybe i'm too cynical. But I've heard too many fall for the AWS is better!, then be startled by their $200-300K/month AWS bills.

**[Wil Sinclair](#679 "2010-11-29 05:24:00"):** With Netflix as the poster child of large-scale AWS success stories, it would surprise me if they are paying the same rates as the rest of us. And if they are getting a 'volume discount,' I wonder how it would affect cost arguments Adrian makes. But setting my own cynicism aside, success speaks for itself. Netflix has not only rolled out a service with computation and data volumes that would make most of us soil ourselves, but scaled it in a way that has kept customers happy and shareholders *very* happy. To trot out the latest figure du jour, Netflix traffic currently accounts for 20% of all internet traffic at prime time. :o I mean really, :o. Great interview, Randy. And hope I catch you at the next Soup Group, Adrian. ;) ,Wil

**[Id](#680 "2010-11-29 05:53:00"):** You are not too cynical, Ops, may be a bit. Everywhere people willing or moving to Cloud accept that data centre is not key to the success of their business. I am yet to see people whose business strategy is intricately dependent on their data centre's competitiveness, migrating to cloud. People like backup, archival service providers or banks whose survival is dependent on cost-competitiveness and security of data [ banking system for example] are yet to sing the 'cloud song'.

**[randybias](#681 "2010-11-29 10:30:00"):** Thanks for commenting. I have to say that when I see a commentary like " ', I stopped reading' " I become very disappointed. The Internet can be a tool for good, or ... Well, let's just say that showing your bias that way certainly makes a casual reader want to dismiss your whole argument. Is that really what you want? I have seen a lot of these numbers and have models showing their efficacy or not. It's not black and white. It's 100% use case driven. Also, when I see most non-cloud datacenter models as counter-examples they don't factor in a huge number of variables as they are typically very simple CapEx equations. OpEx is typically ignored as are a number of other critical issues. That being said, it's clear that many enterprises that have invested heavily in IT and have fairly sophisticated infrastructures will not see the same cost savings (e.g. Financial services companies); however, those are not your typical enterprise. Your typical enterprise is bogged down in legacy gear, processes, and people. If, for your business, running IT infrastructure is a core competency, then by all means do it yourself. If for your business, it's not, then it's a foolish business decision to run it yourself. If this was not the case, then most companies would run their own wireless networks, IP backbones, banks, logistics & shipping, etc.

**[randybias](#682 "2010-11-29 10:58:00"):** I agree that is mostly true; however, financial services businesses are one of AWS' largest enterprise customer segments. I think it's a mistake to assume that cloud is about migrating old applications out. It's about 'moving', not 'migrating'. Netflix is a classic example here. They didn't migrate their existing streaming service out to a new service, they re-engineered it and moved to the new service running on AWS. Cloud usage is largely being driven by new use cases or old apps being re-imagined, not old apps being migrated as-is to someone else's infrastructure. And in this case, many of these enterprises for whom IT is a core competency are even going to AWS. Large financial services organizations use AWS to do massive data processing for public data (e.g. end of day trading data). So, again, it's not a black and white issue. There is definitely value here that is being derived across all industry segments and for all size businesses. Otherwise AWS wouldn't be having the explosive growth it's having.

**[rabbitburns (Mark Gowdy)](#683 "2010-11-29 12:58:54"):** Cloud Innovators: Netflix Strategy Reflects Google Philosophy: http://bit.ly/bZ0ESU

**[neohealth (Raghu Havaldar)](#684 "2010-11-29 15:48:12"):** Maybe it's time that EMRs moved to the Cloud. Here is a good reason why the model needs serious consideration - http://bit.ly/bZ0ESU.

**[Ops](#685 "2010-11-29 20:17:00"):** I prefaced many of my comments with my cynicism. And yes, cynicism, sarcasm and disdain are certainly not the "nicest" way to sway viewpoints. I agree 100% with you that this is fully case driven. But my comments were specifically aimed at the netflix case. Not your usual company/enterprise. And I do believe that Netflix should be an enterprise that *should* heavily invest in its infrastructure/technology. If you want to be a trendsetter and not a trendfollower, it requires agility that is not provided via most public clouds "fit into this mold". If you are your standard two-tier small web-service, you don't tend to care about cache latency between your object cache tier and your backend systems. You don't care about minimizing latency between your query slaves in your distributed search system. etc etc. AWS hides many details that are critical in architecting innovative low latency solutions. I just can't see how this is not critical to netflix. But then again, they may not see themselves as a tech company. Which in my book translates to, a trendfollower. And a recipe to be quickly surplanted. (notice apple is building their own datacenters for their streaming service... they consider this critical to their business... Apple has a decent track record I would think... )

**[Ops](#686 "2010-11-29 20:22:00"):** One issue that I see raised by VC's, but rarely considered by companies that make AWS their whole strategy is, "what's the out strategy?" Where is the viable competitor that provides a balance to AWS's so you are not putting all the eggs in once basket?

**[randybias](#687 "2010-11-30 06:17:00"):** I understand your assertion, but clearly Netflix thinks it is getting tremendous value. As the said, they have unpredictable growth patterns and hence AWS provides tremendous value as the capacity issues can be transferred. It seems clear there is a crossover point where you want your own infrastructure, but in many cases that crossover point is unknown. I would argue that everyone should start on the cloud with new apps and not build out their own infrastructure until their business model stabilizes.

**[randybias](#688 "2010-11-30 06:25:00"):** There are a number of viable competitors, including Rackspace Cloud. It's more an issue of building your system in such a way that it's portable, which I have done several times.

**[Rudy Amid](#694 "2010-12-05 15:40:00"):** Anyone know if Skype uses the cloud? They've just recently announced 25 *million* concurrent users. I think they should be the poster child of cloud computing - if any.

**[eric_brewer (Eric Brewer)](#695 "2010-12-06 08:39:48"):** Old but new to me: Adrian Cockcroft ([@adrianco](http://twitter.com/adrianco)) on Netflix' move to AWS (a big deal): http://bit.ly/bZ0ESU

**[lemire (Daniel Lemire)](#696 "2010-12-06 13:20:54"):** Netflix moved to Amazon's cloud (AWS) http://bit.ly/bZ0ESU (via [@eric_brewer](http://twitter.com/eric_brewer)) -- fascinating analysis

**[theserverlabs (The Server Labs)](#697 "2010-12-06 17:40:09"):** Great interview with Netflix architect Adrian Cockcroft on the flexibility of the cloud http://bit.ly/bZ0ESU

**[Manoj Narayanan](#698 "2010-12-09 02:44:20"):** Interesting to note AC's comment about rendering hardware and underlying services ephemeral. Extending this concept would imply portability of applications across public clouds. Given the commoditized nature, this could very well mean that a new player like Google is one step away from mimicking a new "AWS"? This could also provide a transition path for cautious organizations. Maybe move to a private cloud first, wait for the "protocols" to materialize and do a gradual re-build of your new apps as you move to a public cloud. Question: How would one go about doing the migration if there are critical business dependencies on mainframes? Is it commercially viable for a player - IBM wouldnt have a business rationale to do it - to set up something in cloud? O

**[randybias](#699 "2010-12-16 01:27:00"):** I think it's possible and viable. Not sure it makes sense for IBM. Search for "Mainframe Rehosting" on Google. There is technology out there to enable moving off of legacy mainframe systems with relatively little pain.

**[Gilad](#2311 "2010-11-23 11:05:00"):** Great post! You inspired us to write up a post called "Cloud Computing sells itself", with some follow-on observations. We are seeing customers already bought into the public cloud idea, and asking the follow on questions (such as "how do I make it secure?"). Here: http://www.porticor.com/2010/11/cloud-computing-sells-itself-the-view-from-netflix/

**[Bob Boblaw](#2312 "2010-11-23 19:46:00"):** Randy, can you calculate the fully loaded cost of an hour of compute time in a private cloud? How does that compare to what public clouds cost? In other words is there a private cloud approximation of an EC2 instance hour?

**[randybias](#2313 "2010-11-23 23:10:00"):** Good question, Ray. There is probably a ton of variance. We have some models that I could play with for public providers that might work. Will see what we can do. That would make for an interesting post.

**[Ops](#2315 "2010-11-28 04:20:00"):** The moment I read this... "Our datacenter runs Oracle on IBM hardware, we could have switched to commodity hardware in a datacenter, but skipped that step by going to AWS", I stopped reading. Of course if you outsourced your technology strategy to vendors ( by using oracle rac, instead of thinking your data strategy , and buying the most expensive hardware out there without regards to costs, instead of mitigation of failure with software) then sure, anything will look cheap by comparison. Specially when you then throw OSS into the mix. I have yet to see, any company with any reasonable infrastructure ( which I'm assuming nextflix is one ), which does not reap huge cost savings by having things in house ( the caveat emptor being that it was to be well done). Maybe i'm too cynical, but all I gathered from his answers was; " I don't know how to run operations, so I fell for the dog and pony show". He's saying, I could have run things more efficient, but I didn't. Well, I guess he shouldn't be running operations then, someone else should be hired for that ;) Public Clouds are great for early stage when you don't know your scale. They are also great to leverage for large batch processing. But once you've reached the threshold of the first hundred server instances, their cost skyrockets beyond reason. Last two startups we've trounced public cloud pricing, all while maintaining scalability. But that does require competent staff and good negotiating skills :) Again, maybe i'm too cynical. But I've heard too many fall for the AWS is better!, then be startled by their $200-300K/month AWS bills.

**[Wil Sinclair](#2316 "2010-11-28 22:24:00"):** With Netflix as the poster child of large-scale AWS success stories, it would surprise me if they are paying the same rates as the rest of us. And if they are getting a 'volume discount,' I wonder how it would affect cost arguments Adrian makes. But setting my own cynicism aside, success speaks for itself. Netflix has not only rolled out a service with computation and data volumes that would make most of us soil ourselves, but scaled it in a way that has kept customers happy and shareholders *very* happy. To trot out the latest figure du jour, Netflix traffic currently accounts for 20% of all internet traffic at prime time. :o I mean really, :o. Great interview, Randy. And hope I catch you at the next Soup Group, Adrian. ;) ,Wil

**[Id](#2317 "2010-11-28 22:53:00"):** You are not too cynical, Ops, may be a bit. Everywhere people willing or moving to Cloud accept that data centre is not key to the success of their business. I am yet to see people whose business strategy is intricately dependent on their data centre's competitiveness, migrating to cloud. People like backup, archival service providers or banks whose survival is dependent on cost-competitiveness and security of data [ banking system for example] are yet to sing the 'cloud song'.

**[randybias](#2318 "2010-11-29 03:30:00"):** Thanks for commenting. I have to say that when I see a commentary like " ', I stopped reading' " I become very disappointed. The Internet can be a tool for good, or ... Well, let's just say that showing your bias that way certainly makes a casual reader want to dismiss your whole argument. Is that really what you want? I have seen a lot of these numbers and have models showing their efficacy or not. It's not black and white. It's 100% use case driven. Also, when I see most non-cloud datacenter models as counter-examples they don't factor in a huge number of variables as they are typically very simple CapEx equations. OpEx is typically ignored as are a number of other critical issues. That being said, it's clear that many enterprises that have invested heavily in IT and have fairly sophisticated infrastructures will not see the same cost savings (e.g. Financial services companies); however, those are not your typical enterprise. Your typical enterprise is bogged down in legacy gear, processes, and people. If, for your business, running IT infrastructure is a core competency, then by all means do it yourself. If for your business, it's not, then it's a foolish business decision to run it yourself. If this was not the case, then most companies would run their own wireless networks, IP backbones, banks, logistics & shipping, etc.

**[randybias](#2319 "2010-11-29 03:58:00"):** I agree that is mostly true; however, financial services businesses are one of AWS' largest enterprise customer segments. I think it's a mistake to assume that cloud is about migrating old applications out. It's about 'moving', not 'migrating'. Netflix is a classic example here. They didn't migrate their existing streaming service out to a new service, they re-engineered it and moved to the new service running on AWS. Cloud usage is largely being driven by new use cases or old apps being re-imagined, not old apps being migrated as-is to someone else's infrastructure. And in this case, many of these enterprises for whom IT is a core competency are even going to AWS. Large financial services organizations use AWS to do massive data processing for public data (e.g. end of day trading data). So, again, it's not a black and white issue. There is definitely value here that is being derived across all industry segments and for all size businesses. Otherwise AWS wouldn't be having the explosive growth it's having.

**[Ops](#2320 "2010-11-29 13:17:00"):** I prefaced many of my comments with my cynicism. And yes, cynicism, sarcasm and disdain are certainly not the "nicest" way to sway viewpoints. I agree 100% with you that this is fully case driven. But my comments were specifically aimed at the netflix case. Not your usual company/enterprise. And I do believe that Netflix should be an enterprise that *should* heavily invest in its infrastructure/technology. If you want to be a trendsetter and not a trendfollower, it requires agility that is not provided via most public clouds "fit into this mold". If you are your standard two-tier small web-service, you don't tend to care about cache latency between your object cache tier and your backend systems. You don't care about minimizing latency between your query slaves in your distributed search system. etc etc. AWS hides many details that are critical in architecting innovative low latency solutions. I just can't see how this is not critical to netflix. But then again, they may not see themselves as a tech company. Which in my book translates to, a trendfollower. And a recipe to be quickly surplanted. (notice apple is building their own datacenters for their streaming service... they consider this critical to their business... Apple has a decent track record I would think... )

**[Ops](#2321 "2010-11-29 13:22:00"):** One issue that I see raised by VC's, but rarely considered by companies that make AWS their whole strategy is, "what's the out strategy?" Where is the viable competitor that provides a balance to AWS's so you are not putting all the eggs in once basket?

**[randybias](#2322 "2010-11-29 23:17:00"):** I understand your assertion, but clearly Netflix thinks it is getting tremendous value. As the said, they have unpredictable growth patterns and hence AWS provides tremendous value as the capacity issues can be transferred. It seems clear there is a crossover point where you want your own infrastructure, but in many cases that crossover point is unknown. I would argue that everyone should start on the cloud with new apps and not build out their own infrastructure until their business model stabilizes.

**[randybias](#2323 "2010-11-29 23:25:00"):** There are a number of viable competitors, including Rackspace Cloud. It's more an issue of building your system in such a way that it's portable, which I have done several times.

**[Rudy Amid](#2325 "2010-12-05 08:40:00"):** Anyone know if Skype uses the cloud? They've just recently announced 25 *million* concurrent users. I think they should be the poster child of cloud computing - if any.

**[randybias](#3004 "2010-12-15 18:27:00"):** I think it's possible and viable. Not sure it makes sense for IBM. Search for "Mainframe Rehosting" on Google. There is technology out there to enable moving off of legacy mainframe systems with relatively little pain.

**[Ravi Kalakota](#3007 "2011-01-26 14:30:00"):** I am a Global CIO/CTO and I don't see how large enterprises with a distributed global footprint can compete with the economics of public clouds in the coming years. Based on my experience, it typically costs 6000+ per year to run a physical server (fully burdened commodity WINTEL) and about 3-4,000 per year for a virtual server (depends on utilization). Don't get me started on Storage costs. As data centers get full, the decision for CIOs is - do i invest in another big data center or do I push non-critical apps into Virtual Private Cloud (enabled by AWS). As I lose people because I can't increase their salaries due to corporate constraints - do I replace them or do I leverage AWS where I can probably manage 1000s of images with a few people. Trust me it is a lot less expensive to run on EC2 than operate a Data Center that is running below 50% capacity. Of course not everything makes sense for the cloud. I don't see putting low-latency applications, systems of record (ERP, Supply Chain) or apps that deal with customer private information for a while. But systems of engagement - crm, service, help desk, web portals etc. -- are perfect for the cloud. Also, I don't see why (unless IT is your core competency) you would want to build a multi-tenant platform in-house from scratch when you can leverage Force.com or similar PaaS to give you a jump start. Engineering high quality code/PaaS/apps with offshore teams ( a reality in every global organization) is incredibly hard. We are definitely seeing the 4th wave of computing in the trend line — mainframes, client-servers (pc revolution), and 3-Tier-Web (internet), Cloud (+mobile).

**[randybias](#3008 "2011-01-26 14:45:00"):** Extremely cogent and crisp response to @Ops. I couldn't have said it better myself. Thank you.

**[Nicholas Tang](#3009 "2011-01-27 20:26:00"):** I'm skeptical in some ways, not because of the viability of running an infrastructure in the cloud (very viable!) but because of AWS specifically - their *data transfer* costs are ridiculously high. The killer cost of running S3, for us at least, was not the storage cost but the cost of putting data onto that storage and serving it off. Let's say you have 10TB of data. The cost for that is 14c per GB, not bad. But the cost to get the data into S3 is 10c per GB, almost doubling it. And every time that data goes outbound (i.e. getting served to end users) is another 15c per GB. But Netflix is at scale, ok. At the highest public levels, AWS is 5.5c/ GB for storage, 10c/GB for uploading to storage, and 8c outbound. Even w/ great cache-hit ratios for CDNs, there still have to be massive costs to the actual serving of content. That's what I don't understand about this - how can Netflix afford the data transfer costs unless - unless! - they're getting special pricing or some other special arrangement in exchange for the press. (Another note: we've seen and heard of, from other people, of significant throttling on S3, EC2, etc. when you start doing significant amounts of data transfers. I have to wonder if Netflix has found a way around that, or maybe if they've got a special arrangement where they don't hit it.)

**[Pete](#3074 "2011-10-04 08:21:00"):** Nicholas, Netflix only uses AWS for the encoding of their videos. The cost to get data in is now: Data Transfer IN All data transfer in $0.000 per GBI don't know what it was 8 months ago or over a year ago when the article was written... Netflix probably had a rock-bottom price arrangement though even then. So all their paying for is the transfer of the processed files to the actual CDNs ("We use Akamai, Limelight and Level3 CDN’s for streaming the movies, which is a cloud based service." as the interview replay states). Which is not very much data at all. With Direct Connect which is new but I'm guessing amazon was well informed would be coming or maybe even got in on before it became publicly available, the cost of getting the processed files out of S3 would be even less than 8 cents/gb. To sum up there is no data transfer from any AWS service to netfix's audience, so the bandwidth costs are negligible.

**[Pete](#3075 "2011-10-04 08:22:00"):** Well that's embarrassing their=they're
