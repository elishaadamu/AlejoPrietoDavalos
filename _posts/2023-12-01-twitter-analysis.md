---
author: alejo_prieto_davalos
title: Twitter Analysis [public]
date: 2023-12-01 12:00:00 +0000
categories: [SocialNetworks, Crypto]
tags: [networkx, igraph, mongodb, web_scraping, crypto]
image:
  path: /media/projects/twitter_analysis/graph_followers_cut.png
  height: 100
  width: 100
summary: Twitter analysis for marketing, follower graph, clustering, keywords, metrics, storage in a historical DB.
language: Python
---

# Twitter Analysis | Follows Graph | Trending Topics | Keywords
### (In construction)
- Repository: https://github.com/AlejoPrietoDavalos/twitter_analysis

Using Python I developed a system for trend monitoring and connection analysis for a set of crypto-oriented users of interest.

The system collects data through third-party APIs, stores it in a DB, automatically saving information and timing periodically.

The user can then process that data to extract information and display graphs.



- Graph of followers and following, clustering, keywords and trends that they follow according to their tweets in the last N days.

- For the USA, the Trends are obtained, and then I classify them into more generic Topics using AI.

- For each cluster of users, the associated trends and topics, and the categorized keywords, are obtained.