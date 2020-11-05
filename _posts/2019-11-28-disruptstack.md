---
layout: post
title: DisruptStack - Israeli startups that raised money
feature-img: "assets/img/startups_raised_money.png"
image: /assets/img/disruptstack.png
image_alt: disruptstack
tags: [php-programming-language, laravel-framework]
---
A [web scraper](https://web.archive.org/web/20200614083156/https://disruptstack.com/) for news on Israeli startups that raised money or made an exit.

At first I wrote a PHP script to scrape all Israeli startup news.
I let it filter (using REGEX) for specific keywords in the title and decsription of the articles it finds, so it would only keep articles about startups that raised or exited.

I wrote a simple html/css for it and deployed. The result was a slow webpage that took minutes everytime you wanted to load the page.

At that point I understood that I had to change the architecture of the application.

The solution I found involved separating the scrapping logic from the presentation logic. I would've to use a database for that. And so I started learning about databases.

At that point I decided I would start learning and using Laravel as the framework for the project.

The new game plan I came up with was:

* Run the scraping logic in a task schedualer (cron job) twice-a-day to fetch news.
* Store the scraped data inside a MySQL table.
* Let the presentation logic take data from the database and present it to the viewer.

This way the presentation logic does not need to rely on the scrapping logic to load the page. It made the website blazing fast and a joy to use.

I learned a lot from this project.