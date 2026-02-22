# Veracity chain (draft)

The amount of information every individual has to deal with grows every year. A deeply concerning fact though is that much of this information is misleading or false and it takes a lot of effort even to get to the original source, not to say to check if it is true or not.

For ages our tool to boil down to the truth was the mechanism of reputation. When the source of information is a person and you know him for many years, you can judge how likely you've got the truth. But nowadays the information is rarely clearly associated with a person and there is so much of it that it's quite impossible to know so many persons anyways.

Modern technology created this problem and in the technology we could find a solution. In the same way as search engines made Internet a tool to find any information in a few clicks, we need a tool to check how much we can trust this information. To achieve this, we need a digital system with the clear rules where any actor providing reliable information automatically becomes more trust and any wrongdoer looses it.

## The general idea

In the system Actors make Statements. Actor is identified by his public key. Making a Statement means that the Actor takes some array of bytes, signs it with his private key and publishes it in the blockchain. An existing blockchain like bitcoin could be used for this purpose or some new blockchain could be developed. By means of hashing any digital information (text, photo, video, audio, etc.) could be made to a Statement. In fact, modern cryptocurrencies manage statements about money transfers or smart contracts.

The most important thing about a Statement is that it's existence is publicly verifiable and irreversible. So if at some point some Actor's Statements are found to be false, he will loose his reputation.

The main problem is how to check if Statement is true or false? One of the ways to solve this problem is to use a chain of trust. There should be a mechanism when a Statement of Actor A is verified by Actor B and a level of veracity for the Statement is stored in the same blockchain as a new Statement of Actor B. There should be a mechanism to prise such verifications and when a lot of people will do such work, you can build a veracity chain (a chain of trust) from an original Statement to some Actors who you trust because you know them from outside of the system (like your friends for example or even known experts in the field).

The idea is to build a system which stores some pieces of information and provides you a way to automatically build many different veracity chains from some distant source which provided this information to the known persons or organizations which you trust because you know them in the real life. And also if some Actor is compromised, you can instantly adjust it's veracity level and the system will give you new estimates of the veracity for all information previously verified by this Actor.