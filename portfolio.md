---
layout: page
title: Portfolio
permalink: /portfolio/
---

# Table of Contents

1. [Craigslist-Redux](#craigslist-redux)
2. [NYU Math Finance Group App](#nyu-math-finance-group-app)
3. [Dark-Poole](#dark-poole)

# Craigslist-Redux

---

#### Full-stack, functional, modern recreation of Craigslist

![craigslist 1]({{site.baseurl}}/images/craigslist1.png)

## Philosophy

Why recreate Craigslist? Some may argue that the site is perfect for its functions, as demonstrated by the longevity and relevance of the site. I wholeheartedly agree. I admire the engineers and designers at Craigslist: the site is incredibly complex, yet has great performance and clarity in UI/UX. I rarely hear criticisms of Craigslist for good reasons. The site is truly what the Web should strive for. No frills, all gas.

However, with the emergence of new used goods sites like Grailed, I wished to combine some modern elements of used goods sites like Grailed with Craigslist.

## The Inspiration: Grailed.com

![grailed logo]({{site.baseurl}}/images/grailed.png)

For those unaware of Grailed, here are some reasons why I believe they have been so successful:

- **Minimal and consistent UI/UX**
- **Emphasis on product images:** reading an eBay listing feels like reading technical documentation.
- **Infinite scrolling:** Platforms should encourage browsing and consumption. That simple friction of clicking the "more" button can be the difference between an user that stays for an additional n-minutes.
- **Favorites:** You can add any listing to your personal "Favorites" and keep track of them in one page, and get notifications when prices change. In the same page, you can keep track of sellers you follow.
- **Seller branding:** sellers can add profile pictures and usernames. You can also add profile pictures in eBay, but when do you ever see them? I don't even know if I have a profile picture uploaded on eBay. But I don't know or care since I never come across it.
- **Price drops and bump:** You can perform 2 actions to your listings. Drop the price by n%, or bump the listing to the top every week. Try this very simple action on eBay. Price dropping takes around 10 clicks, and bumping is non-existant.
- **Comments on listings:** Comments allow sellers to broadcast information or answer specific FAQs. Comments also allow buyers to publically broadcast information about the listing. I've had times where I found out the product is fake thanks to comments left by users.

## So it's just a mismash between Craigslist and Grailed?

> Imitation is the sincerest form of flattery

Yes! I truly love the UI/UX of Grailed. I believe the site really set a standard for how product-centric sites should look and perform. When I talked to the co-founder of Grailed in my freshmen year of NYU, I never forgot what he told me:

> I didn't know how to build Grailed when I built Grailed. I just Googled it. Literally. "How do I build a website where I can do this." There's so much knowledge on the internet, that you can figure anything out if you read about it. Some combination of believing in yourself and making it happen.

I internalized the same philosophy building this site. I didn't know the first thing about building a site at this scale. I simply confronted problems as they emerged, solved them by any means necessary, and slowly developed the vision for what the site should look like, feel like, and perform like. Nothing motivated me to build this site than the sake of building a beautiful product I can be proud of.

## Stack

The site uses the MERN stack: MongoDB, Express, React, Node

The site is hosted on Heroku: [https://craigslist-redux.herokuapp.com/](https://craigslist-redux.herokuapp.com/)

The code was linted by the Airbnb ESlint config.

## UI/UX spotlight

#### Location & Category Search

![spotlight 1]({{site.baseurl}}/images/craigslist2.png)

One of the most frustrating user experiences in Craigslist is the location and category filters. For the computer savvy, no problem. However, for the average user, I believe the filters are too fragmented and visually cluttered. Just looked at this!

![bad ui]({{site.baseurl}}/images/craigslist3.png)

Thus, I consolidated the location and category filters in a single section. The products are automatically updated as the user changes the filters in real-time.

#### Product Details Page

![product details page]({{site.baseurl}}/images/craigslist4.png)

The product details page has one clear emphasis: images. In a world where a baseline smartphone has enough clarity to shame DSLRs, I believe product images should be the center of any used-goods site. Good images sell listings! Users can offer or message the seller through the site.

#### Sell Page

![sell page]({{site.baseurl}}/images/craigslist5.png)

The sell page optimizes for simplicity, clarity, and "no more additional steps". One annoyance of posting through Craigslist is the multiple steps you must go through in order to get to a page like this. You must first select your location, then borough, then category, then sub-category... then on and on. In the idealistic world users wish to live in, one consolidated sell page leaves no confusion. If users click submit, users want the listing to be uploaded. Simple as that.

Another sensitive detail: image upload! Users can drag n' drop images, then rearrange them in the order they wish. Many sites allow users to drag n' drop images, but they don't let you rearrange them. If images are presented in a grid before upload, you should be able to drag them to rearrange. Users wish to have easy and intuitive creative control over the presentation.

#### Messages Page

![messages]({{site.baseurl}}/images/craigslist6.png)

In Craigslist, you communicate through anonymous (or not) emails. However, I believe a platform should be self-contained if possible. Email is an asynchronous messaging tool, which can be easily replicated in more conversational format through live chats. Moreover, the email function of Craigslist has been vulnerable to famous exploits such as the brilliant [Airbnb growth hack](https://davegooden.com/2011/05/how-airbnb-became-a-billion-dollar-company/). Thus, I implemented a live chat that allows users to easily categorize messages by products. Moreover, the offer integration allows users to send direct offers without small chat if desired.

#### Seller identity

![seller identity]({{site.baseurl}}/images/craigslist7.png)

What does Craigslist definitely lack? User identity! I understand that the site caters to privacy concerns and ease of use. However, users feel empowered and attach to the online identity they create in each platform. Moreover, it's incredibly useful to know many items the user has previous sold on the platform. Users can customize their username and profile picture. Giving users an "email address identity" is practically worse than giving them none! Of course, unless your email is something like: jack@twitter.com

#### Favorites

![favorites]({{site.baseurl}}/images/craigslist8.png)

Adding a listing to your personal favorites should be as easy as possible to facilitate active engagement and combat fickle memories. I believe if favoriting a listing takes longer than a single click, the user already faces significant friction. Moreover, the user should be able to favorite listings without visiting the details page. All users need to do is toggle the star icon in the listings, then they can acess their favorites in the same layout as other product grids.

# NYU Math Finance Group App

---

#### Valuation and options pricing tools for finance students

![mfg app home]({{site.baseurl}}/images/mfg1.png)

## Philosophy

Finance lives in excel, for good reasons. If you're an industry professional, you rule over excel and excel rules over you. However, in NYU's Finance classes, you are usually working with very rigid excel sheets that you are just plugging inputs into. This is not a commentary on the US undergraduate finance curriculum, so I'll skip extensive flaws with this approach of teaching in many of my classes. However, we believed that we can improve the user experience of using such tools in classroom settings.

Tracking down formulas in excel may be intuitive to the finance student, but it's incredibly disruptive to the overall user experience. Moreover, the formatting issues, circular dependencies, and other quirks make "debugging" a pre-made excel sheet incredibly confusing and unintuitive. In the web, we can signal the users about these issues in explicit ways. Instead of saying "circular dependency error", we can tell the user exactly what field is causing the error. Thus, we believe that the web can be a great candidate to host such calculation and plotting with beautiful UI/UX.

## Stack

The site is built using React (Typescript), Serverless coupled with AWS Lambda: [https://app.mfgnyu.com](https://app.mfgnyu.com)

This is also the first time we've used the GraphQL schema.

## UI/UX spotlight

#### Feature Request

![mfg app feature req]({{site.baseurl}}/images/mfg2.png)

Since we built a platform for undergraduate finance students, we believe that we should create and iterate features most requested by students. Thus, we created an incredibly easy (and anonymous) modal form that can send requests straight into our Slack server.

#### Discounted Cash Flow Calculator

![dcf calculator]({{site.baseurl}}/images/mfg3.png)

A common theme you will notice throughout the features is the clear separation between the inputs and outputs. Although the output can be used to manipulate the input that would result in the specified output, we believe that a clear separation is often lacking in excel sheets at NYU.

Moreover, as a student resource, we believe we should leave no variable or formula to assumption. Every variable and formula should be extensively documented and explained.

#### Gordon Growth model

![GG calculator]({{site.baseurl}}/images/mfg4.png)

Although the previous DCF calculator was a simple calculator, the Gordon Growth model is a well-known valuation tool that benefits from graphical representations. Although we can easily imagine which variables will push the valuation in what direction, we find it hard to imagine the magnitude of the changes. Thus, a graphical representation of the surrounding values can give us an intuitive sensitivites of the different variables.

The graph is interactive, and users can hover over each point in the plot to see what values will result in such valuations. In the web, we have no excuse to present a non-interactive graph. Interactivity in learning tools is an essential feature that encourages exploration and retention.

#### Valuation Model Picker

![model picker]({{site.baseurl}}/images/mfg5.png)

Damodaran's model picker is an incredibly useful and logical tool that allows students to pick the appropriate valuation model for the respective company. However, his excel sheet is essentially a flowchart of questions without extensive validation. We can use the typical web checkout flowchart to present these questions in an incredibly beautiful and validated manner.

#### Black-Scholes Option Pricing Calculator

![black scholes options calculator]({{site.baseurl}}/images/mfg6.png)

The Black-Scholes options pricing calculator is an incredibly daunting calculator for the average student. I'm not particularly terrible at math, but it took me quite some time to truly understand what the model tries to capture and represent.

Thus, we prioritized presenting the inputs and outputs in an coherent and simplified manner. For example, rather than asking for the direct time-to-maturity, we present calendar dates and calculate TTM from the user inputs. Moreover, we present an interactive graph that visualizes the call and put options. In the past, graphical representations of options greatly contributed to my understanding of payoffs. I believe the same pattern will apply to other students.

# Dark-Poole

---

#### Permanent Dark(er) theme for Jekyll

![dark poole landing page]({{site.baseurl}}/images/poole1.png)

Check out the live example: [https://andrewhwanpark.github.io/dark-poole/](https://andrewhwanpark.github.io/dark-poole/)

## Philosophy

I am a big fan of the current wave of the Web moving towards dark UIs. For a nightowl like myself, staring at a white static site at 3 AM through my 27 inch monitor burns holes in my retinas. (Disclaimer: this site is white themed because the site is mainly for photos!)

Jekyll is an incredibly powerful tool to create static sites. Jekyll is markdown-driven, and creating new posts or articles is a fun experience. Moreover, Jekyll has many sites that host beautiful pre-made themes. (Remember wordpress themes? Now you can do it as an adult)

However, I clearly noticed a lack of dark themes. At least good looking dark themes. [Poole](https://github.com/poole/poole) by @mdo is one of my favorite Jekyll themes. (@mdo is also the creator of Bootstrap) Poole actually ships with a dark mode, but the dark mode is only active through CSS media queries and is not... really dark. It's more like "dark blue mode". Thus, I decided to make a new theme based on Poole inspired by Derek Kedziora's site palette. Unlike Poole, the theme will stay dark regardless of the user's preference.

## UI/UX spotlight

#### Archive

![dark poole archive]({{site.baseurl}}/images/poole2.png)

An archive is an essential feature of any respectable blog or static site. Check out [Aaron Swartz's blog arhive](http://www.aaronsw.com/weblog/archive) or [Slate Star Codex's archive](https://slatestarcodex.com/archives/). They are so simple, but you know each and every one of those links will take you on a fantastic journey. These archives emphasize content over all. Similarly, Dark Poole's archive balances simplicity with utility.
