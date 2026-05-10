# Veracity chain (draft)

The amount of information every individual has to deal with grows every year. A deeply concerning fact though is that much of this information is misleading or false and it takes a lot of effort even to get to the original source, not to say to check if it is true or not.

For ages we used personal trust and public reputation as the main tools to manage information. But nowadays it's often a challenge to reliably associate information with a person or public figure. And there is so much information from so many persons and institutions that it's easy to get lost in it.

Modern technology created this problem, but it also could provide a solution. In the same way as search engines made Internet a tool to find any information in a few clicks, we need a tool to check how much we can trust this information.

To digitalize trust, we need a system with clear rules where any actor providing reliable information automatically becomes more trust and any wrongdoer looses it. Let's call such system _the veracity chain_.

## The general idea

Persons, companies and public figures are represented in the _veracity chain_ system as _Actors_ making _Statements_. _Actor_ is identified by his public key and is controlled buy a person, group or institution owning the corresponding private key. A single person or organization may have many independent _Actors_ in the _veracity chain_ which allows them to do a fresh start or make _Statements_ openly highlighting different level of trust.

Making a _Statement_ means that an Actor takes some array of bytes, signs it with his private key and publishes it in the blockchain. An existing blockchain like bitcoin could be used or a new blockchain could be developed. By means of hashing any digital information (text, photo, video, audio, etc.) could be made into a _Statement_. In fact, in cryptocurrencies transactions could be considered as such statements about money transfers.

Thanks to the blockchain properties, any _Statement_ is **public** and **irreversible**. So if at some point some Actor's Statements are found to be false, he will irreversible loose his reputation.

The main problem is how to check if Statement is true or false? One of the ways to solve this problem is to use a chain of trust. There should be a mechanism when a Statement of Actor A is verified by Actor B and a level of veracity for the Statement is stored in the same blockchain as a new Statement of Actor B. There should be a mechanism to prise such verifications and when a lot of people will do such work, you can build a veracity chain (a chain of trust) from an original Statement to some Actors who you trust because you know them from outside of the system (like your friends for example or even known experts in the field).

The idea is to build a system which stores some pieces of information and provides you a way to automatically build many different veracity chains from some distant source which provided this information to the known persons or organizations which you trust because you know them in the real life. And also if some Actor is compromised, you can instantly adjust it's veracity level and the system will give you new estimates of the veracity for all information previously verified by this Actor.

## Economics of truth

Trust and reliable information are key components for many businesses. We trust banks to count our money. Banks trust clients to give them credits. Stakeholders trust companies and buy their shares. Companies trust governments and buy their obligations. So in the modern world **trust equals money** in many cases.

The _veracity chain_ system should be built in a way where providing reliably information equals getting some small economical gain and builds you trust capital. And abusing the system by making false _Statement_ means massive loss of trust capital and massive economic loss. It's like proof of stake, but for general purpose information instead of cryptocurrency transactions.

## Areas of application

There are a ton of possible applications for _veracity chain_ system:
- a browser extension that shows you how much you could trust the news page you are looking
- a filter for social networks and news feeds, reducing disinformation and spam
- a mechanism to reliably verify real-world conditions in smart contracts
- a mechanism to verify trustworthiness of businesses and persons
- new financial tools, which could make loans and corporate shares obsolete
- a way to get real reviews about products and services (filtering out paid reviews)
- fighting spam and DDOS