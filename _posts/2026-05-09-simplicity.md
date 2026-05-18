---
layout: post
title: "The Simplicity Trap: Why AI is making us \"simple\" in the wrong way (or not)"
---
People like to talk about how simple things are.

- "Look at this code I wrote, simple, elegant, just a few new lines and reutilizing an existing framework and it does all the job I need"
- "Check out this magic bash one liner blob. I paste it, and it simply configures everything for me"
- "Claude Code vibed the entire backend of my app in one go, and when I run it, it simply just works"

In engineering, we use "simple" as the ultimate compliment - we want simple systems, simple code, simple deployments, simple everything. But lately, I become to realize that we could be talking about two completely different things when we say that word. And as we lean harder on AI to build things, we are accidentally optimizing for the kind of simplicity that might eventually make our systems, and even our brains, obsolete.

<!--more-->

#### Two flavors of "Simple"

**Conceptual Simplicity** is the first kind of simplicity that typically resonates with most of us. This is the "nifty" stuff - when you spend 3 days thinking to just write ten lines of code that magically achieves all the requirements. It's the art of finding the perfect abstraction, reusing components to their maximum, and keeping the footprint so tiny that the entire logic fits inside your head and can be effortlessly written on a napkin. The solution is simple, it's elegant, but it's hard to get there. It requires understanding all the requirements inside-out, and looking for similarities and pruning the unnecessary until only the crux of the system remains.

**Operational Simplicity**, on the other hand, is the other kind. This is the "just make it work" approach. It's a one-liner bash blob, an inline reimplementation of a library because you don't want to manage additional dependency, or the bitbanging of a protocol just to move data from A to B with the least amount of effort. It's easy to run, and extremely easy for AI to write. But it's often considered "functional slop", as things are probably redundant, bloated, and hard for an average developer to fully comprehend and work on top of.



### But wait, isn't the former just premature optimization?

Normally, when I go all in on optimizing and simplifying the things I implement, I will usually get slapped by this infamous quote by a more senior engineer: "premature optimization is the root of all evil." However, I'd argue this doesn't really apply. I believe this quote applies to improving the system or performance ahead of knowing its true bottleneck, versus designing things to be simple and nifty.

While one could make a statement saying that by doing so, we are effectively "optimizing" for design simplicity, where the bottleneck of a team effectively producing results on top of the repository could be something else (e.g. a bad CI/CD pipeline, too many different deployment scenarios, etc), but let's face it, aren't we always optimizing for something prematurely? If we know the bottlenecks, then we won't have bottlenecks.



### Is software becoming toilet papers?

I was discussing this with a friend recently, and we landed on a rather funny analogy: When you’re writing "nifty," conceptually simple code, you’re treating your software like a cathedral. You care about the patterns, the architecture, and simply the joy of achievement when staring at it. You are building something big but also something simple in principles, like growing a fractal. But if you hold the view that software is just a means to an end, you might ask: **"Is it worth printing fancy patterns on a roll of toilet paper, when you’re just going to use it to wipe and flush anyway?"**

From a purely operational perspective, the answer is no. If the code works and solves the problem now, why spend the brainpower making it elegant? AI becomes the ultimate "toilet paper" manufacturer - it is incredibly good at generating operational blobs that work perfectly in isolation. You ask it for three features, and it gives you three separate stacks. Without prior guidance, it doesn’t care about your elegant abstractions or aesthetics. It just wants to "wipe and flush."

### Bounded Context Windows: Why we embrace Elegance and AI doesn't

This got me wondering: Why do we humans cherish elegance so much in the first place? Is it just because of the natural pride of an intellectual being?

I don't think so. I think it’s biological. Just like LLMs, Human beings have "bounded context windows." Our working memory can only hold about several "chunks" of information at a time. To manage complex systems, we must compress them. **Elegance is our compression algorithm.** By creating a "nifty" abstraction, we turn fifty lines of logic into one mental "chunk." Conceptual simplicity is the only way we can fit a massive system into our tiny biological brains.

AI doesn't really have this problem. Modern LLMs have context windows of millions of tokens. They don't get "confused" by verbose, redundant, or layered code. To an AI, a 500-line nested `if-else` block is just as easy to process as a 10-line recursive function. Sure, it might get lost or its attention scattered across if it looks at too many things at the same time, but it still has the capacity to make sense of everything it ingests.

I think regardless if it's AI or human beings, how we approach solving a problem is the same: **Following the path of least resistance, find a solution to a problem or at least solve part of it within our current context window.**

For us, the way to solve things it to be able to generalize and compress, bear the pricinciples in mind, and only zoom into the particular thing that we want to work on. Since the AI doesn't feel the "weight" of the code, it follows the path of least resistance and embraces **Additive Operational Simplicity.** It just keeps layering more code on top of code.

### What if we cannot make sense of code anymore?

I'm afraid the danger here is that we are drifting towards a world of "Post-Human" software, where we can only interact with codebase with AI's help.

If we stop valuing conceptual simplicity because "the AI can just handle the mess," we are effectively trading away our ability to reason about our own creations. We are building systems that are "write-only"—perfectly functional, but impossible to "chunk" into a human mind.

When we prioritize the "wipe and flush" over the simplicity and elegance, we eventually reach a point of architectural bankruptcy. The "pipes" of our infrastructure get clogged with millions of lines of AI-generated wipes, and because we didn’t spend the energy to keep the system conceptually simple, no human plumber will be able to knock on the pipes and pinpoint the root cause.

### The meaning of the craft

A lot of software engineers find meaning in the "niftiness." We like writing fancy Rust or functional languages that feels intellectually satisfying. Is that a waste of time? Does society just want results?

Maybe. But I believe that guarding the architecture is the last stand of the human engineer. If we surrender to "Operational Simplicity" just because it’s faster, we aren't just losing a hobby—we’re losing our agency.

AI can generate the code, but it shouldn't be allowed to take away elegance. Our job is to guide AI to adhere to a conceptually simple vision of things, even when it’s easier to just let it print more toilet papers. Because at the end of the day, we’re the ones who have to live in the house the plumbing is built for.

---

This post is written in collaboration with Gemini for brainstorming. I swear I still haven't surrendered my agency yet!

