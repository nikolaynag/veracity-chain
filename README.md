# Veracity chain (draft)

The amount of information every individual has to deal with grows every year. A deeply concerning fact though is that much of this information is misleading or false and it takes a lot of effort even to get to the original source, not to say to check if it is true or not.

For ages we used personal trust and public reputation as the main tools to manage information. But nowadays it's often a challenge to reliably associate information with a person or public figure. And there is so much information from so many persons and institutions that it's easy to get lost in it.

Modern technology created this problem, but it also could provide a solution. In the same way as search engines made Internet a tool to find any information in a few clicks, we need a tool to check how much we can trust this information.

To digitalize trust, we need a system with clear rules where any actor providing reliable information automatically becomes more trust and any wrongdoer looses it. Let's call such system _the veracity chain_.

## The general idea

Persons, companies and public figures are represented in the _veracity chain_ system as _Actors_ making _Statements_. _Actor_ is identified by his public key and is controlled buy a person, group or institution owning the corresponding private key. A single person or organization may have many independent _Actors_ in the _veracity chain_ which allows them to do a fresh start or make _Statements_ openly highlighting different level of trust.

Making a _Statement_ means that an _Actor_ takes some array of bytes, signs it with his private key and publishes it in the blockchain. An existing blockchain like bitcoin could be used or a new blockchain could be developed. By means of hashing any digital information (text, photo, video, audio, etc.) could be made into a _Statement_. In fact, in cryptocurrencies transactions could be considered as such statements about money transfers.

Thanks to the blockchain properties, any _Statement_ is **public** and **irreversible**. So if at some point some _Actor_'s Statements are found to be false, he will irreversible loose his reputation.

Most of the _Statements_ in the system will provide information about other _Statements_ (or _Actors_) in the same system, declaring them trustworthy or deceptive (or something in between).

The main issue is how to check if _Statement_ is true or false? The system itself doesn't know anything about the real world and can't magically find the truth. The main idea is that the system can aggregate a lot of information and automate the mechanism of trust we used since the beginning of time, but on the much bigger scale.

One of the ways to solve this problem is to build a chain of trust. Suppose _Actor_ A makes a _Statement X_ about the real world. _Actor_ B verifies this statement and issues it's own _Statement Y_ which declares some veracity level of the _Statement X_. There should be a mechanism to incetintify such verifications. When a lot of people will make such verification, you can build a veracity chain (a chain of trust) from an original _Statement X_ to some _Actors_ who you trust because you know them from outside of the system (like your friends for example or even known experts in the field). And the system can give you some calculated veracity level of the original _Statement X_.

So the idea is to build a system which stores some pieces of information and provides a way to automatically build many veracity chains from some distant source to the known persons or organizations which you trust (because you know them in the real life). And what is very important, automatically take into account any deceptive statements of some _Actor_ to automatically adjust veracity level and obtain new estimates of the veracity for all information previously published or verified by this _Actor_.

## Economics of truth

Trust and reliable information are key components for many businesses. We trust banks to count our money. Banks trust clients to give them credits. Stakeholders trust companies and buy their shares. Companies trust governments and buy their obligations. So in the modern world **trust equals money** in many cases.

In the _veracity chain_ we want to incetintify the following behavior:
- make _Statements_, especially estimating veracity level of other _Statements_
- build level of trust for your _Actor_ and prise it
- avoid deceptive information as much as possible, because it leads to massive loss of the level of trust

The important idea here is the asymmetry of trust: you need to do a lot of true _Statements_ to build trust and just one deceptive _Statements_ completely ruins it. Another important idea is that not all true _Statements_ have the same effect on the trust: the most valuable are contradictory _Statements_ which bring new information to the system.

## Areas of application

There are a ton of possible applications for _veracity chain_ system:
- a browser extension that shows you how much you could trust the news page you are looking
- a filter for social networks and news feeds, reducing disinformation and spam
- a mechanism to reliably verify real-world conditions in smart contracts
- a mechanism to verify trustworthiness of businesses and persons
- new financial tools, which could make loans and corporate shares obsolete
- a way to get real reviews about products and services (filtering out paid reviews)
- fighting spam and DDOS