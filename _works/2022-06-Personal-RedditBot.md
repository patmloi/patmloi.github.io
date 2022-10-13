---
title: Reddit Telegram Bot
organisation: Personal
date: June 2022
duration: Jun. 2022
description: Prevent mindless scrolling by sending the top 3 Reddit posts of a given subreddit to Telegram. 
---

# Context

After scrolling through r/AmITheAsshole on Reddit, then repost accounts on Instagram, I realised that endless scroll on social media led me to exceed my daily limit of tea. I then decided to only read the most scalding cup of tea for my daily entertainment, instead lukewarm tea by the gallons.

# Project Overview

I determined that how over-the-top the drama is could be represented by its number of upvotes, and scraped the top 3 post contestants, as well as the top 3 spiciest takes with Reddit's API. To avoid the endless scroll on social media platforms, the posts were sent to me via a Telegram bot. 

# Demo

![Initialising the bot on Telegram](/assets/images/works/RedditTelegramBot/init.png)

To keep things SFW on this blog, I will be demo-ing with r/aww instead. 

![A Reddit post with an image displayed on Telegram](/assets/images/works/RedditTelegramBot/image.png)

Each post is sent as one message, as combining all three posts and their comments in one message would exceed Telegram's message length limit of 4096 latin characters. Even if the message length limit did not exist, compiling all the content in one message would make it too wordy and difficult to digest.

Media, such as images and video, are sent as via separate message. 

![A Reddit post with a poll undisplayed in Telegram](/assets/images/works/RedditTelegramBot/poll.png)

Reddit's interactive features, such as polls, are not accessible through Telegram. However, the comments, which are hidden on Reddit before participating in the poll, are visible to lurkers on Telegram.

# Challenges 

## Parsing content using Markdown in Telegram

I initially attempted to use Markdown notation to process the Telegram message contents, but encountered inconsistencies between Markdown notation and Telegram's flavour of Markdown. To mitigate this, I attempted both <code>parse_mode='Markdown'</code> and <code>parse_mode='MarkdownV2'</code>, both of which did not address the syntax inconsistencies. 

This error was also encountered by [other users](https://stackoverflow.com/questions/62230148/python-telegram-bot-markdown), and I avoided the error by using HTML parsing instead. This was to avoid syntax confusion when writing future posts. 

# Potential future projects

## Prediction of upvotes based on content 
- Motive: Read the juiciest posts before they become popular. 
- Scope: NLP Models (Sentiment Analysis)
- Blockers: None identified

## Automated Reddit repost account 
- Motive: Sharing the tea (and hopefully earning some advertising side income if the account becomes popular)
- Scope: Image generation (Screenshots / Recreated from post text)
- Blockers: The lack of a publically available Instagram API

# References
- [Create a Telegram Bot](https://sendpulse.com/knowledge-base/chatbot/create-telegram-chatbot)
- [Building a Reddit Autoposter Telegram Bot with Python](https://www.section.io/engineering-education/telegram-bot-python/)
