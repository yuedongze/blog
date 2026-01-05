---
layout: post
title: "Go generate meets vibes: vibe code Go one interface at a time using govibeimpl"
---
Vibe-code Golang one interface at a time.

During the holidays, I was working on a personal project in Go, and I wanted to use AI to help me do a few things (e.g. implement a downloader that downloads a file from Google Drive). However, I'm not a huge fan of having AI IDEs creating new directory structures or introducing abstractions that I need to read through and understand.

<!--more-->

Instead, I thought it would be cool to:

- define an interface that i will need to use
- expect AI to write an impl to that interface
- i can just expect i will receive an instance of that interface at run time
- perhaps i'll need to read about the api contract to see what concrete data types i need to pass in and read out
- profit i guess

And then I thought it would be great to combine this with `go generate` where for every interface i define, i can just attach a `//go:generate` tag so AI can fill in the rest at compile time.

Therefore, I built govibeimpl (https://github.com/yuedongze/govibeimpl), a CLI tool that works with go generate that allows me to tag an interface for AI to implement, and seamlessly integrate that as part of my development flow.
