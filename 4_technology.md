---
layout: page
title: Technology Recommendations
permalink: /Technology/
nav: true
weight: 1
toc: true
---

# Driving Innovation in the Organ Transplant Ecosystem

## Executive Summary

While investigating organ donation coordination, we found there is a clear opportunity to modernize its technical operations to save both lives and taxpayer dollars. 

Within the organ transplant community, people rely on various technical systems. For example, organ procurement organizations (OPOs) across the country each use one of 4 or 5 different programs, which are separate from additional programs used by transplant center staff. There is no key decision maker who controls all aspects of every system end-to-end, so we refer to the whole as the organ transplant ecosystem. 

There is one key tech system, however, known as the UNet℠ platform, through which most important data flows at some point. The UNet℠ system is closed and proprietary, so we were not able to view the coding architecture, but we discovered key insights through extensive user interviews. 

While investigating UNet℠ and the organ transplant ecosystem as a whole, we identified a number of shortcomings and opportunities. 



*   **"Technical Seams" Or Opportunities For User Error And Incorrect Data Entry**  
    Technical seams are places between automated APIs, or computer-to-computer communication, where information tends to get lost or corrupted. When there are unnecessary, human-powered technical seams between computer systems, we create risk for lost or corrupted data.

*   **Closed And Proprietary Systems Block Innovation**  
    Under the current structure, the black box of UNet℠ provides no opportunity for collaboration or outside competition to drive innovation. In this context, the system owner (UNOS, whose funding results from a government monopoly contract) effectively keeps the United States government beholden to them as contractors with their proprietary tech, against the best interests of taxpayers, physicians, and patients. 

*   **Siloed Systems Prevent Thorough Data Analysis**  
    The current "transplant tech ecosystem" contains many disparate systems that each handle their own data. In systems where there are numerous stakeholders, whoever speaks the loudest often gets to determine the next feature built. In more mature technical organizations, to overcome this human political bias, all decisions on what to build next are validated with central data to ensure the expected outcome is achievable.

*   **Too Much Focus On “Feature Releases” Instead Of Iterations**  
    Users we talked to described upgrades specifically on UNet℠<sup> </sup>as patch fixes. They described frequent “feature releases,” built up with PR campaigns that illustrate the lack of a more modernized approach. The more modern approach, iterative development, involves small changes to a small subset of users. When those changes are effective, then a wider release occurs.

*   **Lost Organs From Transportation Issues & Lack Of Tracking**  
    Hundreds of recovered organs have not been transplanted because they were lost or damaged in transit. With the vast improvements in logistics and transportation within the private sector, organs should not be getting lost this way. 

We have recommendations from both a top-down and bottom-up approach to fix the current technological systems to make organ donation, matching, and transportation processes more efficient. 



### Top-Down (Long-term change)

By “top-down” change, we envision federal contracting reform for the OPTN, especially to create more competition and attract a larger, more dynamic, pool of bidders. This process will take time, at least 1–⁠2 years before any new vendor(s) will begin to release technical changes in the system. Under this approach, we recommend the following:


*   Restructure contracts to focus on pieces of discrete domain business logic (see [Strategy for Buying OPTN Tech]({{ site.url }}{{ site.baseurl }}/Buying-OPTN-Tech)).
*   Ensure future OPTN contractors use open-sourced, cloud-based technology from a government approved cloud provider. 
*   Ensure future OPTN contractors adopt modern digital strategy techniques, including iterative development.
*   Create or require a central data warehouse under an OPTN caretaker that enables data-driven decision making, with standardized metrics. 
*   Ensure future OPTN contractor(s) are incentivised to engage public-private partnerships to improve patient outcomes.


### Bottom-Up (Short-term change)

In the “bottom-up” approach, we see startup innovators working in the present ecosystem to move the field forward. This approach depends on whether UNOS begins to work with new startup technologies — which they currently have no incentive to do — and necessitates the following steps: 



*   Allow third-party innovators to create more effective software that meets the needs of OPOs.
*   Require UNOS to create robust application programming interfaces (APIs) that are accessible to a larger group of users. 
*   Instruct OPTN, who owns the data that UNOS has control over, to require UNOS to share data access with third-party innovators who are bringing solutions to the organ transplant ecosystem via the private sector. 
*   UNOS shall be instructed to provide said data at no cost to the qualified third party innovators as this data has been collected, maintained, and paid for under the current contract with OPTN (U.S. Government).

---

## Introduction 

Every day, nearly 100 people on average are saved by organ transplants in the U.S. But another 33 people die while waiting for a new organ. There is a growing chorus of dedicated professionals who believe that the wait list could be reduced and even eliminated for certain organs with simple technological and process improvements. This paper focuses specifically on how technology impacts the organ transplant community and how it could be used to increase the number of successful transplants. 

After examining and exploring the majority of the technical systems employed by the U.S. organ transplant community, there is a clear sense that the ecosystem as a whole has a major opportunity to modernize its technical operations. In this paper, we will refer to any and all technical systems used by members of the organ transplant community as the organ transplant ecosystem. We emphasize the word “ecosystem” to highlight that there are numerous systems at play, rather than a singular overarching system. While there are a few key critical, taxpayer-funded technical systems , there are also many privately funded technical systems in differing stages of maturity. Currently there is no key decision maker that can control all technical aspects of every system from end to end, therefore the term “ecosystem” is the best way to describe all the disparate systems coming together to form a whole.   



### Digital Services Revolution

Major technological advancements in the last 5 to 10 years have led to breakthroughs in the private sector. These same technological advancements have slowly begun to enter into the U.S. government. Innovative and disruptive efforts have and continue to pioneer methods for procuring and implementing the latest technology from inside the U.S. Government. These new efforts all roughly fall under the banner of “digital services.” 

The failure of Healthcare.gov led to a revolution of how the government buys, builds, and maintains technology projects. These digital services efforts have led the effort to better serve the public through innovative technology. One of the key lessons that has come out of the digital services revolution is that we cannot simply spend more money on the processes and techniques that the U.S. Government is used to procuring if they are not working. Instead we must rethink technology ecosystems as a whole. Today's industry leaders build software that is open source and transparent to foster collaboration and innovation. They also keep the end-user central in determining and evaluating what success looks like. Some of these patterns are laid out extremely well in the [Digital Services Playbook](https://playbook.cio.gov), and will be frequently referred to throughout this paper.

Numerous case studies have illustrated the impact of modern digital changes in government tech projects.[^1] These case studies demonstrate that doing things the same way as even a decade ago is not good enough to deliver the technical systems that U.S. taxpayer deserves. In the context of organ donation, poor technology management and systems are leaving Americans to die after years on waiting lists. 

The U.S. government has the opportunity to save thousands of lives and also billions of dollars by updating the organ transplant ecosystem with the proven principles of the digital services revolution. 


## Current State of the Ecosystem

**Figure 1**{:#figure-1}
![Detailed map of governance and oversight in the organ donation process]({{ site.assets_url }}/assets/images/gov-oversight-map.jpg)

[Download the "Governance and Oversight in the Organ Donation Process" PDF]({{ site.assets_url }}/assets/PDF/ODR-Governance_Map_Final.pdf)

Before diving further into suggestions for improving the organ transplant ecosystem, we will first consider the most common systems and actors in play. 


### Health and Human Services (HHS) Health Resources & Services Administration (HRSA)

HHS is the Government agency tasked with overseeing the contract and regulations powering the Organ Procurement and Transplantation Network (OPTN). HRSA is responsible for auditing and ensuring regulatory compliance is met by all actors across the system. Importantly, HHS is responsible for bidding all components of the OPTN contract to an appropriate vendor. 


### Organ Procurement and Transplantation Network (OPTN)

The OPTN was created in 1984 as a means by which the country could maintain a national waitlist of transplant candidates and facilitate organ allocation sharing. It was chartered to have a board for oversight and governance.

Since the OPTN contract was first awarded in 1986, the only organization to hold the contract has been the United Network for Organ Sharing (UNOS).

See [About the OPTN](https://optn.transplant.hrsa.gov/governance/about-the-optn).


### UNOS UNet℠

By the nature of UNOS’s role leading the OPTN, the technological foundation of the “transplant tech ecosystem” exists as a system built and maintained by UNOS trademarked under the name UNet℠. It consists of four separate but interconnected “trademarked” or “service marked” subsystems named Waitlist℠, DonorNet<sup>®</sup>, TIEDI<sup>®</sup>, Transnet℠. These systems act as a hub through which at some point all of the most important data must flow through. 



*   **Waitlist℠** — Used by transplant hospitals to manage information about patients waiting for a transplant. Waitlist is where algorithms developed in conjunction with the OPTN are used to calculate urgency and predicted benefit.
*   **DonorNet<sup>® </sup>**— Provides OPOs the interface to add, update, or delete donor data, execute match runs, and make organ offers. Transplant hospitals use this system to view posted donor information and record organ acceptance and refusal decisions on all organ offers.
*   **DonorNet Mobile℠<sup> </sup>**— Mobile version of DonorNet with a more limited feature set.
*   **TIEDI<sup>® </sup>**— Enables OPTN members to access and complete donor, candidate, and recipient-specific electronic data-collection records which are a series of numerous forms required throughout the transplant process.
*   **Transnet℠<sup> </sup>**— A system for creating labels for packaging and labeling deceased donor organs and specimens for transplant or research. Transplant hospitals use the system to electronically check in and/or match the organ to the recipient.
*   **UNet℠ APIs** — Relatively new, UNOS identifies APIs as a separate product. UNOS states that APIs can be used to interface data about donors, candidates and recipients to and from a validated Electronic Health Record system (EHR) with “validated” open to UNOS’ interpretation. 


### UNOS Tech is a Blackbox

From the start it is important to note that UNOS considers the tech “internals” of their system closed and proprietary. We acknowledge their right to treat their technology as proprietary, **but we feel strongly that this decision goes against modern day best tech practices. We also feel concerned that by keeping their system proprietary, UNOS is** exploiting their position of privilege bestowed by the U.S. Government in a way that blocks outside competition. Without directly working for UNOS and navigating any Non Disclosure Agreements (NDAs), which appear to bar any public disclosures, there is no clear way to know how they architect and build their systems. While it is common for software providers to create proprietary tech platforms, an opaque entity at the center of the organ transplant ecosystem has the effect of stifling innovation and preventing the field from benefiting from advancements happening in the rest of the tech and healthcare industries. It allows UNOS to unilaterally determine what acceptable organ transplant technology looks like.


### Analyzing UNOS UNet℠

From our research, we can deduce the following aspects of the UNOS system:



*   UNet℠ exists primarily in data centers that are maintained by UNOS. This is in contrast to most modern government software that utilizes a commercially available cloud provider certified to run government maintained workloads.
*   Front-end web pages are built using a .NET framework version released in 2012. This interface that is almost a decade old is what all users interact with on a daily basis when using the system. We have been told by users this is not only frustrating, but often leads to increased error rates, using alternative strategies (that are less secure) to get work done, and excessive reliance on phone communications, which can be problematic given the time-sensitive urgency of the organ procurement/transplantation process.
*   The backend of the system consists of multiple RDS databases and traditional server infrastructure that has iteratively evolved without a complete rewrite. Database and API first backend technology systems have changed drastically over the last 5 years with new technologies that increase website performance and allow for more advanced data analysis. If these changes were to occur, it would lead to faster feature development for websites, better APIs for interacting with third parties, and lower maintenance costs.
*   There appears to be high coupling between front-end and back-end systems with a slow movement toward an API-based infrastructure. 

While it is disappointing that there is limited information around the current architecture of the most important system in the “transplant tech ecosystem,” we can still deduce that the system as a whole is nearing a decade behind what is possible in terms of technology. We verified by asking many users of the systems about their experiences. Several stated that it had regular periods of downtime, and felt dated compared to other systems they used on a daily basis. 


### Buying UNOS UNet<sup>℠</sup>
<!-- TODO: check money map link -->
According to those we spoke with in the community, UNOS has refused to provide insight into its systems and has quoted a price of approximately $25⁠–⁠60 million to sell the code back to the U.S. Government — without substantial evidence to support that figure. As a non-profit contractor, they technically have the ability to do this, even though they were entirely funded directly by the U.S. Government and indirectly by users of the system (see [Money Map](#)). Overvaluing code is a common and unhelpful practice in the government that helps contractors hold their position. Furthermore, it is likely that any code received is closely reliant on the existing infrastructure, which is also custom to UNOS. This would be the equivalent to receiving building plans in foreign language, but not having access to any interpreters. Finding people to interpret the plans at this point can cause more issues than just starting from scratch.


### UNOS Controls the Data

UNOS has historically leveraged its standing as the only OPTN contractor to date and not provided access to the data it has collected and holds on behalf of OPTN. This impediment to data access stifles competition as well as innovation and potential public-private partnerships within the organ transplant ecosystem. UNOS at times appears to take the position that they are an extension of the government, using it as pretence to deny the government or other requestors access to the data, and at other times asserting themselves as a private entity innovating to provide services to the government in competition with the private sector. This data access issue gives UNOS an unfair competitive advantage in the marketplace and results in potentially large negative consequences in delaying or denying life-saving innovation for transplant. 

---

>"In 1999, UNOS fought the government about who owned OPTN data. UNOS refused to share data with non-UNOS researchers investigating the effects of existing liver allocation policy. Actually, they wouldn't share data with anyone, even HRSA. The IOM OPTN Final Rule study made clear UNOS did not own the data and any interested researcher should have access. Ultimately, UNOS, the original SRTR contractor, lost that contract because they were unwilling to share data. I don't see how this issue of sharing access to the IT infrastructure is any different." 
>
> __— former HRSA official__

---

### UNOS Labs℠

Another component of the UNet℠ ecosystem is an entity developed recently named UNOS Labs℠, which has a unclear and opaque relationship to UNOS. While marketed as an innovative and independent unit pushing UNOS forward, UNOS Labs℠ touts incremental developments and improvements to existing UNet℠ modules. Many other companies would consider these improvements routine and part of iterative improvement of the system as a whole. An example of this is the Image Sharing hub ([UNet℠ Image Sharing](https://unos.org/news/innovation/national-donor-imaging-hub/). It is questionable to celebrate a commonplace new feature development in a modern tech system as something that is pushing the edge of innovation for the organ transplant ecosystem. 

---

>“It is surprising how little technical information and community engagement exist behind the UNOS platform. Even in very closely regulated industries like EHRs and Banking, we typically see significant open and transparent technical dialogue between platform owners and their stakeholders in order to facilitate technical progress." 
>
>__— Private sector tech leader__

---

**We can’t emphasize enough that lack of transparency in software development protects the status quo. Under the current structure, there is no opportunity for outside competition to drive innovation. The largest tech companies in the world continue to embrace open-source software, shared cloud platforms, and constant innovation. UNOS continues to lag behind with no competition or outside ability to see what is going on inside the black box.**


### OPTN Data Flow

SRTR is a contract awarded by the U.S. government separately from the OPTN contract. The scientists and researchers at SRTR are critical to determining efficacy and issues across the entire organ transplant community. SRTR is responsible for taking the data on organs and transplants from the OPTN contractor (currently, UNOS) and evaluating transplant centers and OPOs on their performance through reports. 

The SRTR is, by design, an independent and objective source for data analysis to improve science and research for the field. The ability to have this data function in an autonomous fashion is imperative — and transparency around practices for SRTR are crucial for its integrity. 

SRTR ingests data from UNOS monthly, and data from numerous other systems like CMS periodically, in order to build a holistic picture around Organ transplants. Simultaneously requiring SRTR to maintain a complex technical system dependent on OPTN data, however, while separating it by a contractual and physical boundary, encourages numerous technical anti-patterns.



*   There is a duplication of effort as UNOS must stage and shift its data to SRTR, and SRTR must prepare to receive and host the data.
*   Data is received in bulk once a month from UNOS and then valuable time is spent ensuring the data has not regressed and is ready for analysis.
*   While UNOS data is theoretically available to the ecosystem and their dues-paying members, UNOS also sells data as Tableau based dashboards to OPO and transplant centers.


### Organ Procurement Organization (OPO) Tech

OPO technology varies greatly between each organization, but ultimately they all employ various digital and analog processes for overcoming shortcomings that flow down from the UNOS UNet<sup>℠</sup> foundational system. We note that the primary technical systems utilized by OPOs for managing cases are privately owned and operated. While there are at least five separate technical systems procured and utilized by OPOs, we chose to highlight and discuss the dominant system in the community, Transplant Connect’s iTransplant℠ software. 

All the other systems suffer from similar shortcomings, leaving many users frustrated with the amount of work and training required to constantly shift between several technical systems to perform basic functions. As an example of how this surfaces, when a transplant center has to make a decision on an organ offer they have to look at multiple screens: the donor info in DonorNet, the candidate ranking info in Waitlist, and then candidate's clinical info in the transplant hospital's EMR. It would be much easier and quicker if they could look at one screen for this info to make the offer decision.

**Figure 5**{:#figure-5}
![An overview of technology used by the organ tranplant community]({{ site.assets_url }}/assets/images/tech-current.jpg)

[Download the "An Overview of Technology Used By
the Organ Transplant Community" PDF]({{ site.assets_url }}/assets/PDF/ODR-Current_Tech_Final.pdf)



### Transplant Connect iTransplant℠

The largest provider of OPO technology is Transplant Connect. The larger community acknowledges that Transplant Connect is closely tied to UNOS in terms of innovation and technical ability, even while it is a privately funded, for-profit company.



*   Transplant Connect acts as a sub-system of UNOS DonorNet℠, allowing OPOs to collect necessary patient data, and, once they are ready, to create a donor record in UNOS DonorNet℠.
*   Transplant Connect has chosen to use the exact same 2012 .NET framework on which UNOS DonorNet℠ runs. This illustrates that the organ transplant ecosystem as a whole is rewarding the status quo. Furthermore, outdated technology systems are increasingly hard to hire for, and require costly and specialized labor to learn the antiquated skills and tools needed to maintain these systems.
*   It is important to note that Transplant Connect does not use machine-to-machine interfaces called APIs to create the donor records in UNOS DonorNet℠. OPOs must export an XML data file from Transplant Connect and manually upload it into UNOS DonorNet℠. However, this only works for a limited subset of fields and users must still go in and correct the fields that were not correctly populated by the XML file. This represents a “technical seam”, creating unnecessary potential exposure of private patient data outside a closed technical system (more on “technical seams” in the following pages).



### Donor Hospitals

By law, donor hospitals are required to notify OPOs upon imminent death of a potential donor. Donor hospitals’ main tool for reporting is utilizing a phone call in a process called ‘referring’ wherein they contact the OPO, transmitting only limited information in order to allow the OPO to start the process of making a determination as to whether the patient is a viable donor candidate. 

Across the community there is a consensus that this process would greatly benefit from automation between the Donor Hospital EMRs and OPO systems — if not directly into the OPTN tech system (see [OPO Best Practices]({{ site.url }}{{ site.baseurl }}/OPO-Best-Practices)). **We believe as automation increases and systems begin communicating directly with each other, rather than relying on human interventions, the organ transplant ecosystem will have decreased “technical seams” and security risks.**

---

>"I'm really glad you mention the possibility of downloading donor hospital EHR data directly into the OPTN system. This would give external researchers the opportunity to analyze donor data. It is a loss that EHR data is currently being downloaded into iTransplant.....it will be wasted there....and more concerning to me....it could give Transplant Connect some degree of control over it .... and that prospect is disastrous." 
>
>__— OPO CEO__

---

### Transplant Centers 

Transplant centers typically use custom-built solutions that work in conjunction with existing Electronic Health Record (EHR) systems like Epic or Cerner. There has been progress in this vertical of the ecosystem, as UNOS has opened up some APIs which allowed Epic to integrate their Phoenix (Transplants) modules directly into UNOS TIEDI<sup>®</sup>. This type of integration is long-overdue and prevents clinicians from having to maintain two separate systems, often manually updating both for every change that occurs. 


### Startup Funded Tech

Particularly in the area of transportation, there is high interest, and private funding with proven logistical expertise focused on improving the challenge of transporting organs. We highlight these startup companies because they have a powerful potential for innovating and pushing the entire organ transplant community forward in terms of technology. Theoretically they can already do this now without having to wait for U.S. Government contracting changes, but only if UNOS enables connectivity by providing startups API access to their government-held data, a proposition toward which UNOS has appeared unwilling. The private start-ups we interviewed are also extremely mission-driven and passionate about improving the state of the ecosystem, often taking it upon themselves to spend enormous amounts of money and time to improve outcomes. Third-party startups fill an important role in augmenting expertise and driving forward comprehensive technical solutions. 

It is important to point out that while these upstarts provide exciting new possibilities for increased efficacy and lower cost, they are still emerging and navigating difficult challenges, like gaining API access (computer-to-computer interfaces) to real time data in UNOS UNet℠. Without efforts to open up this data and break down barriers, innovation will continue to occur slowly within the organ transplant ecosystem, continuing to rely on the established players to deliver change.


## Shortcomings of the Ecosystem

In this section we will highlight just a few of the shortcomings of the organ transplant ecosystem. This is not an exhaustive list, but an attempt to highlight a few issues that presented themselves once we began to dig into how everything fits together. 


### Technical Seams Can Lead to User Error & Corrupt Data 

Technical seams are the places between automated APIs, computer-to-computer communication, where information tends to get lost or corrupted. In the early days of computer software, it was very common for data to get lost or corrupted when it was manually transferred from a physical paper form onto a computer. Over time, those forms transitioned completely onto a computer and the challenge became getting the relevant data securely from one computer system to another. Computers perform this task of transferring data with much higher reliability than any human could achieve.

When there are unnecessary, human-powered technical seams between computer systems, we create risk for lost or corrupted data. We require heavier than necessary processes where multiple users must log into a system to verify that mistakes were not made, and that all systems have matching data. An example of this in the organ transplant ecosystem is that often OPO coordinators will enter data for labs, then a lab technician will also log in to verify the data matches. This points to the urgency of getting things right, since a simple user mistake could mean a lost opportunity for a transplant, or a catastrophic, fatal event for a patient who receives the wrong organ. 


### Closed and Proprietary Systems Block Innovation

Under the current structure, the black box of UNOS UNet℠ provides no opportunity for outside competition to drive innovation. It is important to understand why open source principles create transparency and trust. Additionally, the government should do proper-risk assessment to determine the place for transparency and open source technology, and where opacity is crucial to the delivery of services.



*   By relying on code that exists in the public domain, the organ transplant ecosystem benefits from millions of coders who are constantly improving the quality and security of the software. 
*   If the core software is Open Sourced, the current tech provider is incentivized continuously to deliver a higher quality product or risk a competitor improving on the publicly available code base. 
*   If the government must transition the software, utilizing Open Source libraries increases the likelihood that incoming technologists can understand and familiarize themselves with the code. 
*   Open source software does not mean underlying data generated by a system is public, only the code powering the servers. The servers themselves with patient data are highly secured and protected. 

See [Building and Reusing Open Source Tools for Government](https://www.newamerica.org/digital-impact-governance-initiative/reports/building-and-reusing-open-source-tools-government/)


### Siloed Systems Prevent Thorough Data Analysis

 

The current organ transplant ecosystem contains many disparate systems that each handle their own data. A better solution would be to build a Data Warehouse as a Single Source of Truth (SSoT) with the OPTN technical system caretaker. Data Warehousing technology has evolved rapidly over the last decade, and has become commonplace in the tech community to host massive datasets in near real-time. 

Creating a SSoT goes beyond just consolidating data and making life easier for end users to consume data. Modern tech teams require these SSoTs to drive decision making on which development task(s) should be addressed next. In systems where there are numerous stakeholders, whoever speaks the loudest often gets to determine the next feature built. In more mature technical organizations, to overcome this human political bias, all decisions on what to build next are validated with data to ensure the expected outcome is achievable. 

By embracing data driven decision making, product management teams pore through all available data, make hypotheses about what they expect to happen if a change occurs, then model it to see if it is likely to occur. For example, if a certain web page for entering organ data is often skipped, that data should be available and analyzed to question why this is occuring. After asking users, the team can make changes to eliminate or improve that page. This is a simple example involving a web interface, but, with access to all available organ data, there would be increased opportunities to analyze all systems and make determinations around why certain actions lead to certain outcomes, with a focus on improving the ecosystem as a whole with every decision. 

See [Digital Services Playbook #12 — “Use Data to Drive Decisions”](https://playbook.cio.gov/#play12).


### Too Much Focus on “Feature Releases” Instead of Iterations

Periodically, UNOS will tout upcoming feature changes. These feature changes are often hyped by public relations campaigns that promise major improvements on a future date. 

Modern tech teams, on the other hand, constantly release experiments to see what works, and then scale up those changes when they are successful. They do this by relying on a pattern of Alpha, Beta and Production releases. **These releases are announced to the community in a transparent and public manner in order to make clear what features are upcoming and when any bugs will be fixed in a shared ‘backlog’** where **users can see exactly what the Development team is working on.** We have noticed a pattern where UNOS is not transparent when features are not released, as well as regarding what bugs are currently affecting the system. UNOS does attempt to follow the pattern of releasing software in iterations, but does so in a way that does not keep pace with private industry, where new features are often released in the span of weeks, not months or years. 

Almost every popular modern website is undergoing constant iterative development. By not focusing on messaging around change as a big upcoming positive thing, tech teams can focus on providing constant value in the background, not overcommitting to something that hasn’t even been validated as a positive change. Sadly, when tech teams overpromise, they end up over-allocating resources to deliver the wrong thing, even when so much time has passed that it's not even what the community is asking for anymore. 

Users we talked to described upgrades specifically on UNet℠<sup> </sup>as patch fixes. “It’s like a plumber plugging their finger in the problem. It’s one patch on the next,” said one technician familiar with UNOS’ technical capacity. 

See [Digital Services Playbook #4 — “Build the service using agile and iterative practices](https://playbook.cio.gov/#play4)”.


### Lost Organs from Transportation Issues & Lack of Tracking

A recent study found that hundreds of organs could not be transplanted because of transportation problems.[^2] We live in a world where it’s rare to order an item from an online vendor and not have the ability to track its location in real time with complete confidence in its arrival, which makes an organ lost on its way to a life-saving operation especially shocking. 

Modern logistics problems have already been solved by numerous industries. Organ transportation may be unique in some ways due to the sensitive handling required, but there are industry experts in the form of startups willing to invest heavily in tackling the technology and logistics challenges involved in moving organs. These startups could not only bring the likelihood of losing an organ down to 0%, but could also attach hardware used to track data like temperature, vibration and other relevant data during transit. This valuable logistical and monitoring data, with machine learning applied, results in the standardization of best practices for the movement of every organ in the ecosystem as well as eliminating the outliers. Monitoring and systematizing these factors could help improve patient outcomes post-transplant, and increase patient survival rates by years. 

What's blocking these innovators from competing is that there is no strong force to compel foundational systems, such as UNOS’s, to share the data required to support a logistical platform to monitor and to move organs. The organ transplant ecosystem should continue to welcome and support those willing to make a positive impact in the community as a whole. 

An emerging tech business trying to enter the complex organ transplant ecosystem faces an uphill battle. UNOS and OPOs act as full-service operations and tend to view these startups as competition rather than partners. 


## Recommendations for Improving the Organ Transplant Ecosystem Technology

[The key principles on how to build these better digital services systems are outlined in detail at [https://playbook.cio.gov/](https://playbook.cio.gov/) and we highly recommend reviewing all 13 principles prior to continuing reading.]

It is impossible to predict the exact outcome of what will happen over the next few years in terms of the organ transplant ecosystem. The next few sections will highlight what we believe to be the most effective “top-down” and “bottom-up” approaches for effectively pushing the ecosystem as a whole forward. 

By “top-down” change, we are predicting a situation in which UNOS no longer holds responsibility for technical innovation and it is passed to a new digital services vendor. It is important to note that this process will take time, at least 1–⁠2 years before a new vendor will begin to release technical change in the system. During that bridge period, UNOS will still be the dominant system and have a choice on how much to innovate. 

In the “bottom-up” approach, we see startup innovators working in the present ecosystem to move the needle forward on systems used to transport organs and assist the OPOs in modernizing. The “bottom-up” approach is highly dependent in the short term on whether UNOS begins to work with new startup technologies. Under the current circumstances, UNOS has little to no incentive to allow new technology companies into the space (see [Governance map, Figure 1](#figure-1) and the [Money Map]({{ site.url }}{{ site.baseurl }}/Appendix/#Money-Map)); however, these changes can still have immediate and dramatically positive effects across the system as opposed to the “top-down” approach which will take time to achieve. 
<!-- TODO: check money map link-->

### Top-Down: Govt Digital Services Model


**Figure 6**{:#figure-6}
![Detailed map of how organ technology could be improved in the long term]({{ site.assets_url }}/assets/images/tech-future.jpg)

[Download the "How Organ Technology Could be Improved in the Long Term" PDF]({{ site.assets_url }}/assets/PDF/ODR-Far_Future_Tech_Final.pdf)


There is a consistent pattern employed by digital service companies in terms of effectively working with a government agency to build effective software and technology infrastructure. As referenced earlier, the [Digital Services Playbook](https://playbook.cio.gov/) pattern is the clearest published outline for how this process takes place. We emphasize that successfully implementing this playbook is highly dependent on the government selecting the right vendor which is covered in our [Strategy for Buying OPTN Tech]({{ site.url }}{{ site.baseurl }}/Buying-OPTN-Tech). 

Over the next few paragraphs we will analyze how a digital services team would begin working with the OPTN to start the process of iteratively building the key technical infrastructure the organ “technology ecosystem” deserves. 

We do this in detail to emphasize that while this process may seem longer or more confusing than just procuring existing software, or hiring a traditional non digital services software vendor, it ultimately leads to a better overall outcome for the community. A U.S. Government owned technical system that by design seeks to constantly improve itself and work with end users to build the most necessary features has the highest probability of meeting everyone’s needs and enduring the test of time.

By clearly laying out this pattern, we hope to chart a course for an OPTN capable of hosting and facilitating a digital services element and who consistently meets the needs and delivers value to the end users of the organ transplant ecosystem technology.


### Implementing Digital Services

The below steps can be best summed up by the concept that the U.S. Government should procure iterative processes, not an end product. Focusing on an end product often results in precious time wasted on actors determining whether the product was actually built as was agreed upon contractually. By focusing on the iterative process, it means that the digital services element gets to focus on doing user research, work with all stakeholders to choose what should be built next, and then build it as quickly as possible, before resetting and starting the process over again. 


### First Steps

Once a vendor capable of building digital services has been awarded, the vendor's focus will become developing a strong relationship with the government’s team. 

The digital services provider should operate with the standard members of:



*   **Product** — ⁠ “Product management is an organisational function within a company dealing with new product development, business justification, planning, verification, forecasting, pricing, product launch, and marketing of a product or products at all stages of the product life cycle.”
*   **Design/Research** — ⁠ “UX/UI Designers are generally responsible for collecting, researching, investigating and evaluating user requirements. Their responsibility is to deliver an outstanding user experience providing an exceptional and intuitive application design.”
*   **Technology/Engineering** — ⁠ “A software engineer is a person who applies the principles of software engineering to the design, development, maintenance, testing, and evaluation of computer software.”

These roles are common elements used in the private sector and the specialities taught at coding schools across the world. By utilizing a method of building software that is similar to the commercial sector, it is more likely the government is not building an entirely custom system that is difficult to maintain. This also speaks to the idea that the government is seeking the best talent to implement a process of innovation over time rather than narrow expertise sourced from the existing community. 

The team will focus on developing a relationship with the government and existing stakeholders while not letting any single stakeholder dictate what the system can and should be. The government may act as a stakeholder and a jumping off point to accessing stakeholders across the entire organ donation community, but they are not necessarily leading the process. This phase can take several months, as government teams that have highly bureaucratic operations can hit several roadblocks that must be navigated. 


### Deliver a Minimum Viable Product (MVP)
As outlined in the [Draft Acquisition Proposal]({{ site.url }}{{ site.baseurl }}/Buying-OPTN-Tech#draft-request-for-proposal), the goal is to buy a repeatable process, not technical specifications. At the heart of this process is the goal of improving technology by developing iteratively over time. The team can and should focus on delivering a Minimum Viable Product (MVP). The MVP doesn’t solve the biggest problem or meet everyone’s needs. Instead, it may be a small project that delivers immediate value to the entire community in a matter of weeks, as opposed to the typical timeline of months that it takes UNOS to deliver a feature. 

What’s interesting about focusing on an MVP is that what’s delivered is typically not the most valuable outcome. While building the MVP, the digital services team will navigate several challenges like meeting all stakeholders and conducting user research, building the hosting infrastructure required to serve software, and working through team processes that enable it to move faster in the future. Therefore, the most important outcome is that the team has started the process of becoming good at delivering something of value quickly into the organ transplant ecosystem.


### Continue Building and Steady State

Inevitably, the first delivered feature will be long forgotten in the future as the team iteratively begins to replace the entire existing system with something more modern and efficient. Not only will the quality of the software increase in time, so will the time it takes to deploy something new. Design Researchers will interview new users and stakeholders, diving deeper into what is really needed to cause positive change across the system. 

It is important to note that while it is best to have the code, the digital services strategy takes into account that the existing system may be opaque or simply not worth the time and effort to decipher before beginning the process of building a new system. More important to having the code is the willingness of the existing contractor to provide data or direct access to their systems. 

As opposed to achieving a fixed, contractually agreed upon end state, like the generic “organ transplant software,” the goal of a digital services strategy is to procure a high performing team that focuses on enhancing its process to adapt to whatever the customer needs. While it may take years, eventually the existing system will recede into the background with the newer system taking over all its tasks and constantly adding increased value.


### Bottom-Up: Fostering Innovative Startups

**Figure 7**{:#figure-7}
![An overview of how organ technology could be improved in the short term]({{ site.assets_url }}/assets/images/tech-shortterm.jpg)

[Download the "How Organ Technology Could Be Improved in the Short Term" PDF]({{ site.assets_url }}/assets/PDF/ODR-Near_Future_Tech_Final.pdf)


Even if the above-described top-down strategy occurs at an extremely quick pace, it will take some time for changes to directly impact the system. Waiting for the changes to occur is not the only effective strategy for creating change across the system. 


### UNOS Automated Programming Interfaces (APIs)

We begin by highlighting that the “bottom-up” approach is highly dependent on UNOS working toward opening up their systems through the use of APIs — ⁠ which the current contracting structure provides them no incentive to do, despite the fact that such APIs would enormously benefit both patients and taxpayers by enabling more transplants. These machine to machine interfaces allow third-party developers to directly access real time data in a way that allows them to build usable software for their customers. APIs are extremely common in government and across the private sector, and. a recent initiative at CMS, called [QPP](https://qpp.cms.gov/developers), heavily emphasized the use of APIs with great success. 

While UNOS has made a recent push to create APIs that allow some data to flow directly into or out of UNet℠, they have also taken the stance that they, in their sole discretion, can determine who should or should not have access to the APIs. UNOS has indicated that APIs are only available to “validated Electronic Health Record (EHR) systems.”[^3] An example is the Epic Phoenix module which recently received an update allowing clinicians the ability to log in directly to UNet℠ through the Epic interface and auto-populate TEIDI forms. UNOS should absolutely encourage this type of computer-to-computer automation between their system and other established EHRs, but we believe there are also other customers who could securely and safely connect to the UNOS system.

Compelling UNOS to focus on developing these APIs and releasing them to a wider audience creates a situation where startup innovators can begin to immediately invest their own capital and talent in creating good software. Through our experience, we acknowledge that it takes work to prioritize development over other tasks that may seem more relevant to the development team. For example, UNOS is currently focusing development efforts on improving transportation solutions internally when they could shift efforts to working with third party companies to accomplish this goal in a more efficient manner. 


### OPO Tech is Primed for Innovation

While it creates huge variance and inconsistency, one of the advantages of having numerous OPOs is that they create competition through their choice in what system they use. This competitive marketplace creates the possibility for private investment and other efforts to move faster than the U.S. government. Currently, OPOs have a patchwork of systems to collect data, manually update UNOS UNet℠, and contact relevant parties, often through numerous phone calls that are not tracked nor documented. There is a strong possibility that, by compelling UNOS UNet℠ to open up APIs, a startup vendor could move toward technological consolidation of all these processes. 

Currently, it is difficult for any startup company to develop software knowing that they won’t have access to relevant data piped directly into their systems. This makes it especially burdensome for the OPO to transition to a new system and manually re-enter all relevant data. 

In order for this innovation to occur, we strongly encourage the government entity overseeing the OPTN contract, which is currently HRSA, to direct UNOS UNet℠ to prioritize enabling third party software development by requiring UNOS to create robust APIs accessible to a larger group of users. This would allow third party innovators to create more effective software that meets the needs of OPOs. 


### Transportation and Logistics

Probably the most promising area of the organ transplant ecosystem ready for disruption focuses on the transportation of organs after they have been recovered. Already-established companies are vying for the opportunity to move organs safely and efficiently across the United States, and bring a bevy of industry logistics experience and top tech talent expertise to solving this problem. OPOs have also shown interest in working with these upstarts, at least implicitly acknowledging that existing systems for transporting organs are not working. 

While it would be impossible to quantify the outcome of how these upstarts could change the system, it is important to note that they encourage the use of iterative development outlined by the digital services strategy above. They have a strong incentive to enter the market with established transportation systems and to work tirelessly to meet the needs of the customer. These upstarts should be supported and encouraged by the government, as they have the potential to bring solutions more rapidly to the market and save lives. 

The key to “bottom-up” change is to encourage innovation by fostering open competition. For too long, the organ transplant ecosystem has had limited technology options . To foster innovation, APIs should be opened to a wider audience, and the wider community should look to these innovators to solve existing problems rather than relying on legacy entities which are not keeping up with the times.


## Overall Key Recommendations

While we can’t dictate what a final OPTN technology RFP would look like, there are some universal modern digital service best practices that most [government technical procurements](https://docs.google.com/document/d/152JhGtgEL5Yorm_Oni_c2aNljSxRTwbO6yV5vYp3FW0/edit#) should follow. 



*   Use an open-source software development framework to power the Front-End web interface.
*   Remove barriers to entry and incentivize innovation within the organ transplant community, including via private entities and/or public-private partnerships.
*   Create a decoupled system with API first development.
*   Adopt Cloud Computing from an established government approved cloud provider (AWS, GCP, Azure)
*   Iterative development instead of purchasing a fixed product.
*   Restructure contracts to focus on pieces of discrete domain business logic.

<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
     [https://khn.org/news/how-lifesaving-organs-for-transplant-go-missing-in-transit/](https://khn.org/news/how-lifesaving-organs-for-transplant-go-missing-in-transit/) 

[^2]:
     [https://unos.org/technology/unet/](https://unos.org/technology/unet/)
