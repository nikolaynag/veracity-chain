# Veracity chain

> This document describes the Veracity Chain concept, first published by [Nikolay Nagorskiy](https://github.com/nikolaynag) in February 2026. The project is in early-stage development. It presents the original formulation of the idea and is intended to evolve through discussion, experimentation, and further refinement.
>
> Last updated: 23 August 2026 ([source on GitHub](https://github.com/nikolaynag/veracity-chain))

## Introduction

The amount of publicly available information grows every year. Fact-checking is not free and sometimes it can take considerable effort just to find the original source of a claim, let alone establish its credibility. At the same time it is very cheap to spread misleading, manipulative or outright false information.

Historically, we have relied on personal trust and public reputation to assess the credibility of claims. But this model does not scale to today’s information environment. There are simply too many sources, individuals, and institutions for us to know them personally or keep track of their reputation and history of their claims.

As it already happened earlier, the technology could help us to scale and provide tools to find a solution. Just as search engines transformed the Internet and blockchain enabled decentralized finance, we cat build a system that will bind claims to sources, registers users trust and calculate sources credibility.

The idea is to create the **Veracity Chain**: a system based on blockchain principles where every claim is permanently bound to a source, or "Actor". Actors who consistently provide reliable information build credibility within the system, while those who repeatedly provide false or misleading information lose it. Credibility becomes a measurable economic asset, creating incentives that make it unprofitable to produce and spread misinformation at any significant scale.

## Technical basis

Two fundamental concepts of the Veracity Chain are _Actors_ and _Claims_.

An _Actor_ is similar to a Bitcoin wallet: a public cryptographic identity controlled by a corresponding private key. An Actor may represent a person, group, organization, or institution. A single person or organization may control multiple independent _Actors_ within the Veracity Chain, allowing them to start with a fresh credibility record or make _Claims_ with different credibility levels under identities with different levels of accumulated trust.

A _Claim_ is a piece of information or an assertion that is digitally signed by an _Actor_'s private key and registered on the blockchain. An existing blockchain such as Bitcoin or Ethereum could potentially be used for this purpose, or a dedicated blockchain could be developed. In fact, cryptocurrencies already use blockchains to record transactions, which can themselves be understood as claims about financial operations.

Using cryptographic hashing, virtually any digital information - including text, photographs, video, or audio - can be uniquely referenced and registered as a _Claim_. The _Claim_ itself is always public, while the information referenced by the Claim may be public or private.

Thanks to the properties of blockchain, every _Claim_ is public and immutable. Once an _Actor_ has made a _Claim_, it cannot be erased or altered. If a _Claim_ is later found to be false, the _Actor_'s history remains permanently associated with that Claim, and their accumulated credibility can be reduced accordingly.

## The chain of trust

The main issue is how to check if _Claim_ is true or false? The system itself doesn't know anything about the real world and can't magically find the truth. The main idea is that the system can aggregate a lot of information and automate the mechanism of trust we used since the beginning of time, but on the much bigger scale.

One of the ways to solve this problem is to build a chain of trust. Suppose _Actor_ A makes a _Claim X_ about the real world. _Actor_ B verifies this statement and issues it's own _Claim Y_ which declares some veracity level of the _Claim X_. There should be a mechanism to reward such verifications. When a lot of people will make such verification, you can build a veracity chain (a chain of trust) from an original _Claim X_ to some _Actors_ who you trust because you know them from outside of the system (like your friends for example or even known experts in the field). And the system can give you some calculated veracity level of the original _Claim X_.

So the idea is to build a system which stores some pieces of information and provides a way to automatically build many veracity chains from some distant source to the known persons or organizations which you trust (because you know them in the real life). And what is very important, automatically take into account any deceptive statements of some _Actor_ to automatically adjust veracity level and obtain new estimates of the veracity for all information previously published or verified by this _Actor_.

## Economics of truth

Trust and reliable information are key components for many businesses. We trust banks to count our money. Banks trust clients to give them credits. Stakeholders trust companies and buy their shares. Companies trust governments and buy their obligations. So in the modern world **trust equals money** in many cases.

In the _veracity chain_ we want to reward the following behavior:
- make _Claims_, especially estimating veracity level of other _Claims_
- build level of trust for your _Actor_ and prise it
- avoid deceptive information as much as possible, because it leads to massive loss of the level of trust

The important idea here is the asymmetry of trust: you need to do a lot of true _Claims_ to build trust and just one deceptive _Claims_ completely ruins it. Another important idea is that not all true _Claims_ have the same effect on the trust: the most valuable are contradictory _Claims_ which bring new information to the system.

One more key idea is that there should be an economical bridge to the real world. The _veracity chain_ system should operate some kind of cryptocurrency with some real-world economic value. It should be possible to invest some real-world money into boosting your trust level, because it provides a stake and makes this trust level valuable. Also having high trust level could mean to be paid more by other actors to verify the statements. This is very similar to the proof-of-stake system in the modern cryptocurrencies.

## Areas of application

There are a ton of possible applications for _veracity chain_ system:
- a browser extension that shows you how much you could trust the news page you are looking
- a filter for social networks and news feeds, reducing disinformation and spam
- a mechanism to reliably verify real-world conditions in smart contracts
- a mechanism to verify trustworthiness of businesses and persons
- new financial tools, which could make loans and corporate shares obsolete
- a way to get real reviews about products and services (filtering out paid reviews)
- fighting spam and DDOS

Perhaps the most promising product built on the _Veracity Chain_ could be a messaging platform with public groups - providing a communication model similar to Telegram, Signal or X, but enriching it with the reputation, credibility and accountability mechanisms of the _Veracity Chain_.