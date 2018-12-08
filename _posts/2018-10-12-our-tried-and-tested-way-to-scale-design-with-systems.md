---
title: "Our tried and tested way to scale design with systems"
date: 2018-10-12 16:17:57 +1100
layout: post
category: blog
tags: design
related_image: /public/images/canva-banner.jpg
---

Below is an excerpt from an [article I wrote on the Canva blog](https://product.canva.com/scaling-design-with-systems/). I go deep on how we address product design challenges related to scale.

<!--more-->

For context, I’m the product designer of the team responsible for creating features that enable Canva users to publish their designs to various “endpoints”, such as social networks and online services.

---

In the past, every time our team identified a valuable endpoint to integrate, say for example, Twitter, it would be designed and implemented in isolation. Once complete, we would identify the next endpoint, say LinkedIn, and start the process again.
As a freelance consultant in a previous life, I saw many businesses, from small to blue-chip clients, facing a similar challenge. A steady pipeline of new features would be requested, designed and implemented one at a time, giving the false benefit of short-term progress, but in turn creating burdens of duplicate designs and code cruft.
The vision of an overall system and feature pattern was lost, and the wheel was reinvented each time a new feature was added.
There are many problems with this kind of process, such as:

* **Resource-heavy:** starting the design process from scratch for many endpoints is time-consuming, costly and inefficient.
* **Legacy documentation:** creating new design artefacts for every individual endpoint results in duplicate screens, making design updates a nightmare, increases the likelihood for mistakes and maintenance becomes a real problem.
* **Code cruft:** when designs are communicated to engineers one endpoint at a time, bespoke code is often created rather than leveraging shared components, thereby contributing to maintenance and performance issues.

Taking inspiration from the age-old manufacturing process, we looked into whether we could identify commonalities within our endpoints and design a universal "mold", allowing us to rapidly ramp up production.

### Building a design task flow
![Task flow - publish to social media and cloud storage]({{site.url}}/public/images/canva-blog-flow.gif)
> This diagram describes how users publish their design to any social network or cloud storage endpoint. New endpoints are usually able to be integrated with little or no changes required. Here you can see before and after a Facebook API update. This shows how well designed systems can be easily updated to accommodate changes in third-party APIs.

*Continue reading:* [Our tried and tested way to scale design with systems – Product at Canva](https://product.canva.com/scaling-design-with-systems/)