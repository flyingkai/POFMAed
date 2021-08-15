# POFMA'ed Dataset Codebook

[TOC]

## Introduction: What is POFMA'ed?

POFMA is the **Protection from Online Falsehoods and Manipulation Act**. It is also commonly known as Singapore's Fake News legislation. The law came into effect on 2 October 2019.

Overviews of the POFMA legislation can be found here:

- [POFMA in the Singapore Statutes](https://sso.agc.gov.sg/Act/POFMA2019)
- [Singapore Legal Advice's Guide to POFMA](https://singaporelegaladvice.com/law-articles/singapore-fake-news-protection-online-falsehoods-manipulation/)
- [Academia.sg's overview of POFMA's news coverage and their statements on POFMA](https://www.academia.sg/pofma/)
- [POFMA'ed explainer infographic](https://pofmaed.com/explainer-what-is-pofma/)

POFMA'ed is a dataset which aims to record every instance of the use of this legislation, for reference by academics, media practitioners and the general public. It will be updated continually.

This dataset began as part of a discourse analysis research assignment for my university. I have published it online because I believe it might be of interest to others who, like me, were searching for more information on the legislation's use. As a student, I would greatly appreciate any suggestions for improving this dataset.

This dataset is maintained by [Teo Kai Xiang](https://twitter.com/teo_kai_xiang). If you have any comments, corrections, or suggestions, please direct them to POFMAed@gmail.com

This dataset is available on [POFMAed.com](https://pofmaed.com).

---

## Version Control

This dataset uses [calendar versioning](https://calver.org/) as its versioning convention. The version scheme is as follows: **YYYY.0M.0D** (Year, Month, Day)

The most recent version and past versions can be found on the dataset's Github Repository.

---

## Sources and Coding Procedure

> The data for each case has been entered manually, using the following sources. The dates on which these sources were last accessed is recorded in the Source Access Date variable (see below).

The POFMA'ed dataset uses the [POFMA Office Press Releases](https://www.pofmaoffice.gov.sg/media-centre/) and [Gov.sg Factually Articles](https://www.gov.sg/factually) for all data other than actor type and accessibility status. The sources used for each case are specified under the Source variables.

To determine the accessibility status of each electronic communication which has been subject to POFMA legislation, the dataset uses media reports, direct sources (the electronic communication itself) or government press releases.

To determine the actor type for each use of POFMA, the dataset uses the target actor's self-identification, via the electronic communication subject to the POFMA usage or other communications by the target actor.

---

## Unit of Analysis: Reports, Uses and Communications

> The following units of analysis are used. The dataset distinguishes between Reports, POFMA Uses and Communications.

**Report.** Each Report of POFMA legislation's usage released by the government (via a POFMA Office Press Release) is given a Report number. Note that a Report can describe multiple POFMA uses, affecting different electronic communications.

**POFMA Use.** Each use of POFMA legislation (a direction or order) is given a POFMA Use number. Note that a single POFMA direction or order can apply to multiple communications.

**Communication.** Each distinct electronic communication which has been subject to a use of POFMA legislation is given a Communication number. Note that a single electronic communication can be subject to multiple uses of POFMA legislation.

> **Why the distinctions?**
>
> The distinctions are necessary because of how a single Report can describe multiple uses of the POFMA legislation, each of which could affect multiple distinct Electronic Communications.
>
> For example:
>
> - According to Report 1, a Facebook post is the subject of a Correction Direction, issued to Individual A.
> - According to Report 2, this same Facebook post is also the subject of a Targeted Correction Direction, issued to Facebook.
>
> This dataset would thus track that Facebook post as **one Communication**, subject to **two distinct POFMA uses**, according to **two distinct Reports**.

---

## Recorded Variables

### Sources

> These variables describe the sources used for each case.

**POFMA Office Press Release.** This variable contains a link to the POFMA Office Press Release announcing this usage of the POFMA legislation.

**Factually Article.** This variable contains a link to the Gov.sg Factually Article which outlines the Falsehoods and Additional Clarifications for this usage of the POFMA legislation.

**Accessibility Source.** This variable contains a link to the source used to verify the accessibility (see below) of the electronic communication subject to this usage of the POFMA legislation.

**Date.** This variable records the date on which the POFMA Office or relevant Ministry issued the POFMA direction, according to the POFMA Office Press Release.

**Source Access Date.** This variable records the date on which the sources named were accessed for data collection.

---

### Legislation Use Variables

> These variables describe each use of the POFMA legislation.

**Source of Request.** This variable records the Minister which requested the POFMA direction, as indicated by the POFMA Office Press Release.

**Type of Direction.** This variable records the type of POFMA direction issued, as indicated by the POFMA Office Press Release. The following categories are used.

- *Part 3 Direction: Correction Direction.* According to the POFMA Office: A Correction Direction is a Direction issued to a person who has communicated a falsehood (i.e. the recipient) that affects the public interest. It requires the recipient to publish a correction notice, providing access to the correct facts. The Direction does not require the recipient to take down their post or make edits to their content, and does not impose criminal sanctions.
- *Part 3 Direction: Stop Communication Direction.* According to the Singapore Statutes: A Stop Communication Direction is one issued to a person who communicated the subject statement in Singapore, requiring the person to stop communicating in Singapore the subject statement by the specified time.
- *Part 4 Direction: Targeted Correction Direction.* According to the POFMA Office: A Targeted Correction Direction is a Direction issued to an Internet Intermediary (“II'), whose service was used to communicate a falsehood that affects the public interest. The Direction requires the II to communicate a correction notice by means of its service to all users in Singapore who access the falsehood through its service. This is so that users who see the falsehood on a platform also see the correction notice on that platform.
- *Part 4 Direction: General Correction Direction.* According to the POFMA Office: A General Correction Direction is a Direction issued to prescribed Internet Intermediaries, prescribed telecom and broadcast licensees, and/or prescribed permit holders of the Newspaper and Printing Presses Act that would require them to communicate, publish, broadcast or transmit a correction notice to their users in Singapore.
- *Part 6 Direction: Account Restriction Direction.* According to the Singapore Statutes, the Account Restriction Direction is a Direction to counteract inauthentic online accounts and coordinated inauthentic behaviour.
- *Access Blocking / Disabling Order.* This category covers all directions or orders which disable access to specific content, such as access blocking orders, disabling directions and disabling orders. According to the Ministry of Communications and Information: The Access Blocking Order requires internet access service providers to disable access for end-users in Singapore to the online location where the falsehood was communicated. Access Blocking Orders apply to situations of non-compliance for other directions.

**Communication Description.** This variable records the electronic communication subject to this use of the POFMA legislation. 

- Each electronic communication receives a unique description with the following scheme: *ACTOR*, *MEDIUM*, *CONTENT*, *ID*. For example: *Actor A Facebook Post 2.*

**Medium of Communicated Content.** This variable records the medium through which the electronic communication subject to this use of the POFMA legislation occurred. So far, the following categories have been used.

- *Facebook*
- *Website*
- *Other Social Media (HardwareZone Forum)*

---

### Actor Variables

> These variables describe the recipient actors involved in each use of the POFMA legislation.

**Individuals Involved.** This variable records, where applicable, the individuals named in the POFMA Office Press Release as the intended recipients of the POFMA direction.

**Organisations Involved.** This variable records, where applicable, the organisations named in the POFMA Office Press Release as the intended recipients of the POFMA direction. This includes internet intermediaries that are not the authors of the falsehoods outlined by the sources used.

**Source Type.** This variable records whether the involved actors were the original source of the claim indicated by the POFMA Office Press Release or Gov.sg Factually Article using the following categories:

- *Primary.* The communication was the original source of the claim indicated by the POFMA Office Press Release or Gov.sg Factually Article.
- *Secondary.* The communication was a re-shared version of the claim indicated by the POFMA Office Press Release or Gov.sg Factually Article.
- *Intermediary.* The organisation was the intermediary for the claim indicated by the POFMA Office Press Release or Gov.sg Factually Article.
- *Unknown.* This type is used when it is unclear whether the actors involved are primary or secondary sources.

**Relation.** If the Source Type is Secondary or Intermediary, this variable explains the actor's relationship to the primary source.

**Actor Type.** This following variables record the type of actor based on affiliated group, using the target actor or their affiliated group's explicit self-identification. The types used are non-exhaustive and non-exclusive, allowing for categorisation of a single actor under multiple categories.

The following dichotomous variables are used:

- *Internet Access Provider*. Entities which provide internet access. For example, this includes telecommunications firms such as Starhub or M1.
- *Social Media Platform*. Entities which provide social media services. For example, this includes firms such as Facebook or Twitter.
- *Media.* Public groups and figures that disseminate news and information to the general public. This includes print, broadcast and digital media outlets; and the journalists or other media workers associated with them.
- *Political Group or Figure.* Public groups and figures that are engaged in activities with explicitly political and partisan goals, such as attaining public office or forming part of the government. This includes politicians and political candidates; political parties and their members; and other partisan groups.
- *Civil Society Group or Figure.* Public groups and figures which are distinct from business and government, and are engaged in collective activism towards common interests. This includes non-governmental organisations; civil society movements; and civil society activists.
- *Private Individual.* Individuals who are not public figures and are not explicitly affiliated with any organisation.

---

### Content Variables

> These variables describe the contents of each electronic communication subject to a use of the POFMA legislation.

**Falsehoods.** This variable records the Falsehoods indicated by the Gov.sg Factually Article. If there is no corresponding Factually Article, the Falsehoods are taken from the POFMA Office Press Release.

**Additional Clarifications.** This variable records the Additional Clarifications indicated by the Gov.sg Factually Article. If there is no corresponding Factually Article, Additional Clarifications are taken from the POFMA Office Press Release.

**COVID-19 Related.** This variable records whether the communication is related to the 2019-2020 COVID-19 Outbreak, as indicated by the POFMA Office Press Release or Gov.sg Factually Article.

**Accessibility Status.** This variable records whether the electronic communication subject to this usage of POFMA legislation is still accessible. Only cases classified as Primary or Secondary sources (see: Source Type) have an Accessibility Status (Intermediaries are excluded). The following categories are used:

- *Accessible.* This electronic communication remains accessible online.
- *Inaccessible (Disabling Order).* This electronic communication is inaccessible due to a disabling order.
- *Inaccessible (Access Blocking Order).* This electronic communication is inaccessible due to an access blocking order.
- *Inaccessible (Removed).* This electronic communication is inaccessible due to its removal.
- *Unknown.* This electronic communication cannot be found by the dataset author, but may still be accessible online.

**Accessibility Note.** This variable records, if applicable, an explanation of the accessibility status of the electronic communication.