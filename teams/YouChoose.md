#The  Project

**YouChoose enables users to gain back control over their YouTube recommendations.**

## Problem

**Algorithms are the gatekeepers** of YouTube.

The various search and recommendation engines select [more than 70%](https://www.journalism.org/wp-content/uploads/sites/8/2020/09/Many-Americans-Get-News-on-YouTube-Where-News-Organizations-and-Independent-Producers-Thrive-Side-by-Side.pdf) of the content viewed on the platform.

Yet, these opaque systems have serious drawbacks:
* They favor clickbaity and sensationalist content
* They are not accountable and hardly customizable
* Their results are confined within YouTube.com

**➜ An AI with misaligned interest decides most of what people watch.**

## YouChoose

**Gain back control over your recommendations** on YouTube.

YouChoose allows you to choose your recommendation model on YouTube.com, including:

* From your content creators
* From other websites and social media feeds
* From alternative recommendation engines like Tournesol.app

**YouChoose helps you design recommendations that are optimized for you, not for YouTube.**

## Motivation


There is a **growing frustration** on the monopolistic influence platforms have in shaping information flows.

**Content creators** are at the mercy of an opaque AI which favors engagement over quality.

**YouTube users** have their attention monetized and pushed towards addictive consumption patterns.

**Regulators** are demanding more AI transparency and market competition. 

**Algorithmic platforms** like YouChoose will soon emerge, similar to how app stores offered alternatives to native applications.

YouChoose is an early **attempt to end the era of algorithmic monopolies**.

A step toward a **more open and decentralized internet**, with more user agency.

## Our approach

**YouChoose is an alternative recommendation system** for YouTube.

Rather than purely relying on AI, **YouChoose leverages human expertise** to identify the best related content. 

Such specialized human expertise is found among:
* Content creators (main feature)
* Volunteer contributors [Tournesol.app](https://tournesol.app)
* Existing online communities (feeding recommendations from Reddit / RSS feeds)
* Users' personal feeds on other platforms (Facebook)
 

## Unique Value Proposition

**For YouTube users**:

* Recommendations that are aligned with your own interest, not someone else's profit.
* Seing recommendations outside of YouTube, including wikipedia pages, articles or links to other platforms.
* Gaining back agency over your informational diet and choosing who you trust to recommend you content
* Super light habit change: Simple extension which overrides recommendations directly on YouTube.com.


**For content creators**:
* Gain back control on the other videos your content promotes.
* Gain a new direct connection to your audience, through recommendations.
* Get analytics on the recommendations and ads which YouTube puts on your content
* Find out if some of your videos are being shadow banned


## Fostering quality contributions from the community

In a second stage, it seems natural to also enable the community to curate recommendations.

For a given video, a user could suggest another a video or an external link that is relevant.

There needs to be incentive mechanisms to reward quality contributions, as curation is time-consuming. On the other hand, their needs to be safeguards to prevent spamming. 
One approach is to use a blockchain based coin. 

In order to make a content recommendation, users would need to stake some tokens. 
When the recommendation is downvoted by the community, the staked tokens are lost, and redistributed to the people whose recommendations have been upvoted. 


# The Technology

## Stack

* The main tool revolve around a browser extension which can parse and modify the HTML on youtube.com. 
It is implemented in Javascript, and works both on Chrome / Chromium / Brave and FireFox.

* From the extension, a dashboard can also be opened on the user's browser to allow them to add recommendations for specific videos.
At first, this is aimed for content creators to customize their own content.

* The extension and dashboard communicates with a backend server from which the cuztomized recommendations are fetched and updated. 
The backend is implemented in nodejs with a mongo database.



## The Repos


### Exension
 - [YCAI](https://github.com/tracking-exposed/YCAI)
 - The user facing browser extension
 - Contains the content creator dashboard
 
### Backend
 - [YouTube Tracking Exposed](https://github.com/tracking-exposed/yttrex/tree/ea9db843f42977bb652052e10fba2b79de5ded88)
 - Backend infrastructure to collect and parse youtube HTML.
