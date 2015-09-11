---
title: "The 'Cloud' Is NOT Outsourcing"
link: http://cloudscaling.com/blog/cloud-computing/the-cloud-is-not-outsourcing/
author: randybias
description: 
post_id: 451
created: 2009/07/30 15:13:17
created_gmt: 2009/07/30 22:13:17
comment_status: open
post_name: the-cloud-is-not-outsourcing
status: publish
post_type: post
layout: post
category: cloud-computing
---

# The 'Cloud' Is NOT Outsourcing

There was recently a small brouhaha on twitter regarding whether a 'private' or 'internal' cloud is really a 'cloud'.  There was a very high level of chatter including a ton of the clouderati such as [@jamesurquhart](http://twitter.com/jamesurquhart), [@samcharrington](http://twitter.com/samcharrington), [@boblozano](http://twitter.com/boblozano), [@jesserobbins](http://twitter.com/jesserobbins), [@ITKLcameron](http://twitter.com/ITKLcameron), [@samj](http://twitter.com/samj), and many more.  The argument of the folks who claim that internal clouds aren't **really** clouds is best [summarized](http://twitter.com/GeorgeReese/status/2895192297) by [@GeorgeReese](http://twitter.com/GeorgeReese), who essentially said clouds must be: 

  1. Virtualized
  2. Outsourced
  3. Utility Charge Model (pay by the hour, with no contracts)
My purpose in this particular post is not to pick on George.  He's a super sharp guy, who literally wrote the book on [Cloud Application Architectures](http://oreilly.com/catalog/9780596156367/) (with an Appendix by yours truly).  George has a point of view that is worthy of consideration; however, I disagree with it and I want people to understand why internal clouds are still 'cloudy'.  More importantly, I'd like them to know that internal clouds are going to be where some of the biggest game-changing in the cloud computing space happens.  **The Problem with the Outsourcing Argument** The fundamental issue with the outsourcing argument is the perspective viewpoint.  It's best summed up, again by @GeorgeReese as "[not my problem](http://twitter.com/GeorgeReese/status/2895495010)": 

> @samcharrington Not having hardware or assets to manage is the most interesting part of the cloud (not my problem)

What I think George means here is that from the perspective of the cloud consumer a primary value proposition of the cloud is that it abstracts and hides away the details and pains normally associated with delivering these services.  He argues this is why you can never have an internal cloud, because you own the hardware, you must deal with the 'pain' associated with managing those assets, both operationally and fiscally. This is where the argument breaks down.  If I'm a developer in a departmental team inside a large enterprise and I can go to either a public cloud or an internal cloud and the experience is just the same then from my perspective they are both clouds.  Both are "not my problem". One can argue that from the perspective of that particular business it's clearly got ownership and as an entity that means their internal cloud is 'not cloud', but if we spend only a few seconds looking at this it breaks down quickly: 

  * What if the 'internal cloud' is run by someone else (like IBM)?
  * What if it's part of a separate business unit that is spun out into a separate business?
The notion that outsourcing is special about cloud is wrong, but the notion of "it's not my problem" is spot on. **It's Not My Problem** Perhaps one of the more interesting arguments of the anti-"internal cloud" crowd is the "it's not my problem" claim.  I think this is just another way of saying '[self-service](/blog/cloud-computing/clouds-are-inherently-self-service)'.  Again, as is becoming a mantra for me, self-service means on-demand, pay-as-you-go, and use-only-what-you-need.  The consumer of cloud services does not want to deal with the pain of running the service itself.  They simply wish to consume those cloud services quickly and efficiently. _This holds true whether the cloud is internal or external._ **What Problem Does the Internal Cloud Solve?** There is an imminent issue for large enterprises around how they deliver IT services internally.  The problem is that they are now under increasing competitive pressue from external services such as public clouds and Software-as-a-Service (SaaS) offerings.  This trend will continue, but it's extremely unlikely that the CIO and internal IT folks are going to give up the ghost and walk away from their jobs.  It means that they are going to get competitive instead. Many vendors, right now, are gearing up to deliver offerings that will allow IT departments to deliver competitive internal cloud services, including VMware's vCloud, EUCALYPTUS, Nirvanix, ParaScale, and many, many more.  CIOs everywhere are already engaged in evaluating and understanding these new software packages that they can use for internal cloud offerings and yet this is simply the tip of the iceberg.  It's imminent that enterprises (and others) will adopt these technologies and capabilities in order to remain competitive. So what is the problem the internal cloud solves?  As a wise person ([@samhahn](http://twitter.com/samhahn)) once said to me, there are only a couple of reasons someone buys a new product: to get a promotion or to keep their job.  Internal clouds allow CIOs to remain relevant and IT departments to compete against external services.  _This is a great thing!_ ... and from the internal enterprise consumer's perspective, it's still "not their problem". **(Re)defining Cloud** I'm certain to provoke more controversy with this since so many folks can't agree on what 'cloud' is.  Originally, I was inspired by a hallway conversation turned [blog post](http://news.cnet.com/8301-19413_3-10249486-240.html) of James Urquhart's assertion that cloud is really "just an operational model". For me there are two aspects to this operational model: one from the perspective of the consumer and one from the perspective of the cloud operator. From the perspective of the consumer, any cloud service is a self-service offering that they can consume as they desire.  Meaning that there is minimal or no lock-in.  They can pay as they like (utility pay-by-the-hour model, pay one year in advance, use a PO, use a credit card, etc).  There are no or minimal contracts so they can leave any time.  The services consumed this way are always on-demand and the consumer can get up and going with little or no interaction with a human.  In effect, _consumers get i__nstant gratification_. From the perspective of an operator, clouds must be highly automated, requiring minimal operational overhead.  How else can they deliver the self-service that their consumers desire?  If you need to pick up the phone to call a sales person the operator has #failed.  If you need to spend a week reading the documentation, the operator has #failed.  As on-demand services, clouds **must** be delivered in a highly automated and relatively[1] easy-to-use fashion. Those are the two aspects of the cloud operational model in my mind: 

  1. self-service operational model for consumers
  2. highly automated, low opex, operational model for operators
**The Sum of the Parts Argument** Jumping back to the earlier twitter thread, George Reese, in particular, argued that while outsourcing, virtualization, and the utility charge model aren't individually 'cloud', together they are more than the parts and create a 'cloud'.  Hopefully my definition above rings true with you.  If it does, then it's clear how adding these three components together doesn't create a cloud. Virtualization is simply a means of creating [multi-tenancy](/blog/technology/virtualization-is-not-the-answer-for-clouds) in clouds.  People like Google and Salesforce.com don't use virtualization at all.

## Comments

**[mrbuelow (MrBuelow)](#196 "2009-07-30 22:41:00"):** Please RT: [@randybias](http://twitter.com/randybias) The ';Cloud' Is NOT Outsourcing http://tinyurl.com/lt9ls9

**[John Polgreen](#197 "2009-07-30 22:44:05"):** Great treatment of the subject. The Federal government is already using the cloud extensively, and much of this usage is internal. Much of their reasoning revolves around security and privacy, in addition to the factors you mention.

**[randybias](#198 "2009-07-30 22:57:10"):** @John Polgreen Thanks for your comment John. Please share more information if you can. I would love to learn more about what the government is doing.

**[esturkana (esturkana)](#200 "2009-08-01 11:59:12"):** The ‘Cloud’ Is NOT Outsourcing http://bit.ly/14MJym

**[James Watters](#201 "2009-08-02 01:39:49"):** Ok so I guess James U loves this so I'm interested. I think its a good defense of the necessity of competition in the cloud world--in this case between roll your own and outside providers. Got it--esp with Eucalyptus why not compete? Agree! What REALLY worries me is that we aren't talking standards in this discussion. What keeps me up at night is the fragmentation of cloud development models and how some misguided enterprises might go for the overkill button yet again in making their own clouds which end up being incompatible with other providers. Are interface/api/architecture standards important to anyone else here or is it just me? I think its a simple point to say you can compete internally to provide those standards--but its a HUGE problem if you say you are going to create your own. With projects like Boto and Libcloud there will be an increasingly important ecosystem of cloud tools (built on standards). I'm not trying to be alarmist--but I know for a fact that many big banks during the grid era spun their wheels for a long time rolling their own standards..etc. Thanks @wattersjames

**[randybias](#204 "2009-08-02 15:17:45"):** @James Watters Thanks for such a thoughtful and well written response. I think what is missing is that, at least in the enterprise, there won't be a fragmentation. It's going to be all VMware all the time. There is still no credible contender to the upcoming vCloud product and I've looked at everything in a fair bit of detail now. I say this as someone who would far prefer to see an open standard. Regardless, a de facto standard for enterprise clouds will mean that hosting providers who also use vCloud will have the possibility for very strong integration to internal enterprise clouds. In fact, I have a large blog posting I'm working for just this subject. The real fragmentation you outline will exist more within the public clouds realm than the enterprise. Interface/API/arch standards are very important to me. That's why I released the GoGrid API under an open license, which then caused Sun and RackSpace to follow suit. It also inspired a lot of the work on the OCCI (Open Cloud Computing Interface) API. Absolutely agree with the thrust of your comment, but don't think these dangers actually exist. Enterprises are going to adopt vCloud. There's nothing else on the horizon for them. A de facto standard (like the Cisco IOS command line interface) is, practically speaking, as good as any open standard.

**[James Watters](#207 "2009-08-03 11:46:26"):** @randybias Interesting, I've been talking to VMware a fair amount and I want them to really sparkle on vCloud not just persist in their virt domination. I'll watch for your vCloud blog.

**[davesmithcloud](#208 "2009-08-04 03:28:39"):** The leading figures in Cloud Computing are converging in London this year to discuss the key issues for the future of the sector. Don’t miss your chance to discover how IT and technology decision makers can benefit from this exciting trend. More details here: <http://www.businesscloud9.com/summit>

**[Call Center Philippines](#212 "2010-03-17 19:17:45"):** This is an awesome information presented in a clear, concise manner. What amuses me about the cloud computing concept is that it can be viewed as the current version of timeshare computing - which dates back to the dark ages of computers. All of the benefits of cloud are the same as those touted by timesharing. The difference is the multitude of applications and a sexier name! -Tina

**[Outsourcing Tech Support](#213 "2010-04-15 20:21:42"):** With cloud, people expect flexibility and more innovation through their whole contract term. Outsourcing is tied to the infrastructure and equipment itself. In cloud, you’re delivering an SLA-based outcome. You buy once, and you’re not expected to buy it over again, and you just get new functions. The core is continuously upgraded and you buy around the edges of the core. With cloud, you’re delivering your customers a timeless data centre. It is always at the point in time that technology is at.

**[Inbound Call Centers](#214 "2010-05-03 19:47:22"):** Many enterprises are intrigued by the possibility of reducing IT costs by replacing existing in-house services and resources with lower cost cloud-based resources and services. The combination of the current economic situation along with claims of raw IT services at pennies an hour is driving much of the initial interest in using the cloud as a replacement for private IT infrastructure. What we've seen is that when enterprises inquire about "cloud computing," they are usually interested the associated benefits that cloud promises and may not realize the alternatives available to deliver similar results.

**[KPO Services](#215 "2010-08-04 22:47:03"):** Cloud-based services will radically change the outsourcing business from the service providers' perspective. There will be many more complexities involved in a provider offering to "take over your IT software and hardware and move it to our environment" because cloud-based services with a variety of vendors will comprise a large component of the buyer's IT.

**[Wes](#216 "2010-11-22 18:53:00"):** Cloud computing is not leading to outsourcing? Uh-huh. Did the local bakery compete with Walmart? Cloud computing will result in the transfer of virtually all business information to machines running in Asian countries. My advice: learn to grow potatoes.

**[randybias](#217 "2010-11-22 19:05:00"):** That wasn't the argument. I recommend reading more carefully.

**[Indian](#219 "2010-11-24 09:39:00"):** Amazon has Data centers in the US, Europe, Singapore. It is not only in Asia.

**[Call Center Philippines](#2175 "2010-03-17 19:17:00"):** This is an awesome information presented in a clear, concise manner. What amuses me about the cloud computing concept is that it can be viewed as the current version of timeshare computing - which dates back to the dark ages of computers. All of the benefits of cloud are the same as those touted by timesharing. The difference is the multitude of applications and a sexier name! -Tina

**[Outsourcing Tech Support](#2188 "2010-04-15 20:21:00"):** With cloud, people expect flexibility and more innovation through their whole contract term. Outsourcing is tied to the infrastructure and equipment itself. In cloud, you’re delivering an SLA-based outcome. You buy once, and you’re not expected to buy it over again, and you just get new functions. The core is continuously upgraded and you buy around the edges of the core. With cloud, you’re delivering your customers a timeless data centre. It is always at the point in time that technology is at.

**[Inbound Call Centers](#2190 "2010-05-03 19:47:00"):** Many enterprises are intrigued by the possibility of reducing IT costs by replacing existing in-house services and resources with lower cost cloud-based resources and services. The combination of the current economic situation along with claims of raw IT services at pennies an hour is driving much of the initial interest in using the cloud as a replacement for private IT infrastructure. What we've seen is that when enterprises inquire about "cloud computing," they are usually interested the associated benefits that cloud promises and may not realize the alternatives available to deliver similar results.

**[KPO Services](#2275 "2010-08-04 22:47:00"):** Cloud-based services will radically change the outsourcing business from the service providers' perspective. There will be many more complexities involved in a provider offering to "take over your IT software and hardware and move it to our environment" because cloud-based services with a variety of vendors will comprise a large component of the buyer's IT.

**[Wes](#2303 "2010-11-22 11:53:00"):** Cloud computing is not leading to outsourcing? Uh-huh. Did the local bakery compete with Walmart? Cloud computing will result in the transfer of virtually all business information to machines running in Asian countries. My advice: learn to grow potatoes.

**[randybias](#2304 "2010-11-22 12:05:00"):** That wasn't the argument. I recommend reading more carefully.

**[Indian](#2314 "2010-11-24 02:39:00"):** Amazon has Data centers in the US, Europe, Singapore. It is not only in Asia.

**[outsourcing](#3015 "2011-02-16 11:13:00"):** Pretty good post. I just stumbled upon your blog and wanted to say that I have really enjoyed reading your blog posts.

**[Asphalt Paving](#3020 "2011-03-17 18:36:00"):** Outsourcing is tied to the infrastructure and equipment itself. In cloud, you’re delivering an SLA-based outcome. You buy once, and you’re not expected to buy it over again, and you just get new functions. The core is continuously upgraded and you buy around the edges of the core. And cloud is still developing a new functions. so do you think clouds are like outsourcing/

**[Software Consulting](#3023 "2011-03-28 13:00:00"):** Interesting read, I must say that the cloud is usually associated with downsizing the hardware and saving the capital expendatures. That is what it is all about, isn't it? Moving to the cloud is primarily a software jump or integration that involves less hardware and IT personel. An internal "cloud" seems to me to be counter productive in the spirit of the cloud. Unless you plan to become a provider and then ramping up the hardware is worth the investment. I may be missing something Randy. Thanks for the post.

**[randybias](#3024 "2011-03-28 13:35:00"):** Thanks for your comment. This posting is almost two years old now. I would recommend some newer blog postings such as: http://cloudscaling.com/blog/cloud-computing/elasticity-is-not-cloud-computing-just-ask-google And: http://cloudscaling.com/blog/cloud-computing/debunking-the-no-such-thing-as-a-private-cloud-myth
