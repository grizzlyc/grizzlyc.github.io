---
title: Godaddy LLM Lessons
description: Review of Godaddy lessons learned from using LLMs 
slug: godaddy-llm
date: 2025-08-16 00:00:00+0000
image: cover.jpg
draft: false
categories:
    - LLMs
    - blog
    - review
tags:
    - llm
    - review
    - lessson
weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---

GoDaddy has a gem of a blog post on lessons learned while building Large Language Models(LLMs) in production. 

I think there are a lot of key take aways but one that is particularly catching is how they use an agent for RAG rather than using the user's direct input.

The conversations with the customer are categorized by the LLM. They have a conversation with the customer and try to narrow down what's the issue. From there the LLM knows how to supplement its context with the right information, using a RAG system search.

They state there are two essential patterns in a Retrieval-Augmented Generation(RAG) implementation.

1. Including dynamic content to aid in the customization of the prompt behavior.
2. Providing content relevant to the conversation.

You can add and supplement updated information to the context. From this the LLM can modify its own context. 

By having the LLM control when to make searches on the RAG System, the relevancy of the information is normally improved.

fi a system uses the user's raw input, it's likely to mudy the context. Godaddy observed users would exchange pleasentries before getting to the issue. 

So how do you ensure these are improvements? Presumably, these improvements are verified through evaluations(evals). I have much to learn.





