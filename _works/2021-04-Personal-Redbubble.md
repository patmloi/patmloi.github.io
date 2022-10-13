---
title: Sticker Design Automation
organisation: Personal
date: Apr. 2021
duration: Apr. 2021
description: Generates a sticker design, as well as post title and tags to be used on Redbubble, a Print-on-Demand (PoD) platform. This system has helped me post hundreds of listings, with 1000+ sales to date.
---

# Context

After seeing one too many passive income ads, I decided to pursue my own stream of passive income. However, I was broke and wanted to start something with no initial capital, and something to start quickly just to test the waters. I then discovered Print on Demand services (PoD), which only required me to create and upload designs. I wanted to see if I could automate that process, and that's how this process came to be!

# Project Overview

![My total number of sales on Redbubble](/assets/images/works/Redbubble/Sales.png)
This project ended up way more successful than I expected, with 1000+ sales to date. 


I initially thought that the bulk of this project would be centered around automating processes, but quickly realised that there was more to running an online store - such as product research and interacting with customers.

# Generating text-based designs 

## Pixel Speech Bubble

Using Python's requests library, I sent a POST request with the desired quote to nowhere other than [pixelspeechbubble.com](https://pixelspeechbubble.com/). I also avoided spamming my Downloads folder by customising the destination path.

```
{
    test: "uwu"
    animated: "false"
    orientation: "left"
}
```
A sample POST request.

## Custom fonts 

After looking at too many speech bubbles, I wanted to increase the variety of stickers offered in my shop. I created text images with the Python library pillow, with customisable font, size and colours. 

# Running a Redbubble Shop

## Product Research 

1. New collections

    ![Google Trends No. of Searches](/assets/images/works/Redbubble/GoogleTrends.png)
    When I hear about a new fandom in the same category as existing collections, I compare its popularity to those of existing collections on Google Trends. 

    Using this example of Amphibia, a Disney animated series, I compared it to another series that I already made stickers for, The Owl House. The number of searches for Amphibia consistently remained at about half of The Owl House, even when both shows released a new season in May. 

    ![A Table of Popular Tags on Redbubble](/assets/images/works/Redbubble/PopularTags.png)
    I also look for new fandoms to join on [Redbubble Popular Tags](https://redbubble.dabu.ro/redbubble-popular-tags), which displays the top 10,000 searched tags on Redbubble each week. I restrict my search to the top 1000 search terms, to ensure that there is enough demand for my products in the current and upcoming weeks. I also specifically look for search terms with less than 2000 results, as this would mean the lower probability of similar sticker designs, and lower competition overall. 

    In the above image, entry 204 would meet these requirements.

    ![Top topics and blogs on Tumblr](/assets/images/works/Redbubble/Tumblr.png)
    Due to the list being only updated once a week, I also check the top topics on Tumblr, a fandom-dominated microblooging site. This is updated daily, and allows me to catch new updates.

2. Expanding existing collections

    ![Top 5 Visited Product Pages](/assets/images/works/Redbubble/GoogleAnalytics.png)
    When deciding to include more stickers for an existing collection, I used Google Analytics to determine the most popular stickers, determined by the number of page visits. I shortlist the top 5 items, and look for more quotes by the character, or related quotes within the same conversation. 

3. Specific requests
    ![A Request for a Specific Quote](/assets/images/works/Redbubble/Request.png)
    I occasionally also receive requests for specific quotes in existing collections, which are fulfilled within 3 working days. 

## Customer service

Since product printing and shipping are handled by Redbubble, product quality and delivery issues are not a concern for me. However, I still want to make sure that the stickers with my designs would be high quality, which I ensured by doing some [research](https://pisnak.com/redbubblestickers/) before making Redbubble my chosen platform. 

# Challenges 

Even after streamlining the process of creating the stickers, I faced multiple bottlenecks that prevented me from scaling up the project.

## Sticker content 

The largest time sink was searching for new content. Searching for specific quotes was a manual task, which includes searching for quotes by characters on wikias. If there are no quotes on the Wikia page, or if the page is not updated, searching for quotes becomes even more time-consuming - I would go through text-based social media platforms such as Reddit and Tumblr, and watch highlight reels posted on Youtube. 

## No publically available Redbubble API

Posting the product listings was the other non-automatable task, due to the lack of a publically available Redbubble API. Although creating a new listing eventually only took me 1 minute, the time adds up when posting many listings (50+). 

# Conclusion

I eventually decided that selling merchandise was not a pursuit worth chasing, due to the scaling bottlenecks I faced and the low profit margins that come with a PoD platform. But who knows? Maybe I'll decide to start a new e-Commerce store.

# References 
A huge thank you to [Passive Marie](https://www.youtube.com/c/PassiveMarie), who helped me get started!

