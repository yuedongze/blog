---
layout: post
title: "I built the fastest AI app builder that I can find"
---
A lot of times I use GenAI to quickly prototype something like an app idea or a UI/UX mock for a site. I'd like this text-to-UI experience to be as fast as possible to quickly iterate.

<!--more-->

I've tried classic LLMs like ChatGPT/Claude/Gemini and dedicated text-to-app builders like Lovable/Blink/Bolt/Replit. For the former the experience is still a bit crude - a lot of times I have to manually spin up the pages they create to see what's going on. The latter looks fancy but requires a sign up, and then by the time I enter the prompt, the spinner spins forever to bootstrap a production ready app with databases and log-in, when my intention is just to use it myself and see if it works.

So after I sign out from work yesterday for Christmas break, I decided to vibe one myself and hence created Vibe Builder. The idea is simple:

- Single page HTML. TailwindCSS. HTML components and JS blocks. No need to create fancy frameworks or templates when you can just vibe on DOM elements.
- Build the app where you enter your prompt. Zero deployment hassle.
- Stream everything, never wait for AI to fully finish their thought.
- Optimize for time-to-first-UI-change. You get to se the changes live.
- And post on [HN](https://news.ycombinator.com/item?id=46376987) to see if it works.

This is just a V1, as you can see it only generates dead UI. but i already had fun asking it to generate wild app ideas or clones of existing apps and see how fast AI puts things together.

Next, I'm considering using HTMX to add interactivity to the components, as well as have a vibe API router that actually handles interaction.

Let me know if it builds the app you have in mind!

Link to the site: https://vibes.higashi.blog/
