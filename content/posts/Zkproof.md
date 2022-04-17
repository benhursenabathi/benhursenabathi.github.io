---
title: "How can Zero Knowledge Proof be used by Designers to Design for Privacy"
date: 2022-04-16T15:59:28+01:00
draft: false
---

## Zero-knowledge Proofs
### Zero knowledge proofs have been used to make the information that is exchanged on the blockchain anonymous and private.

Zero knowledge proofs are mathematical proofing system where the prover (the party who has to prove something) to the verifier (The other party who would verify the statement) without conveying additional information.

![Anonymous person with Guy Fawkes mask](https://benhur.me/img/Zkproof/Cover.jpeg)

The statement being conveyed has to only consist of the fact that the prover knows or possesses the secret rather than telling the whole secret to the verifier or any other third party. 

The below diagram from chain link blog represents Zero-knowledge proof protocol and how it works. 
![Example depicting the use of zero knowledge protocol system](https://benhur.me/img/Zkproof/Zkexample.png)

A conceptual example to intuitively understand proving data in zero-knowledge is to imagine a cave with a single entrance but two pathways (path A and B) that connect at a common door locked by a passphrase. Alice wants to prove to Bob she knows the passcode to the door but without revealing the code to Bob. To do this, Bob stands outside of the cave and Alice walks inside the cave taking one of the two paths (without Bob knowing which path was taken). Bob then asks Alice to take one of the two paths back to the entrance of the cave (chosen at random). If Alice originally chose to take path A to the door, but then Bob asks her to take path B back, the only way to complete the puzzle is for Alice to have knowledge of the passcode for the locked door. This process can be repeated multiple times to prove Alice has knowledge of the door’s passcode and did not happen to choose the right path to take initially with a high degree of probability.

After this process is completed, Bob has a high degree of confidence that Alice knows the door’s passcode without revealing the passcode to Bob. (Example Source: [chainlink blog](https://blog.chain.link/what-is-a-zero-knowledge-proof-zkp/)

## A simpler example
Let’s us say, that my grandmother has a secret family recipe. My cousin is  visiting me for the weekend and he claims that he knows the recipe. My grandmother is curious as to how he could know the recipe and asks for it when three of us are in the room. My cousin does not want to tell the whole secret recipe out loud and he tells her “adding 1/2 teaspoon of chilli after mixing the third item”  

This is highly specific and my grandmother (the verifier) asks for more proof as she thinks he might have been lucky. Then my cousin goes on to say that at step 7: you set the temperature to 325°C and reduce it to 225°C after step 9. Again, these are highly specific statements but do not give out additional information like what ingredients are added and the probability of this being a fake statement is lower and lower with more details being added. This convinced my grandmother (the verifier) to verify that my cousin knows the whole recipe indeed. 

Mathematically, Zero knowledge proofs can never be 100% correct but is good enough at 99.99%.

## Where can ZK Proofs be used in Designing next generation digital products?
ZK proofs are used by certain blockchains. What this means is that, you don’t see this in action in real-time but they happen in the backend protocol protecting your data or making you anonymous on the blockchain. For more examples, check out Z-cash where they use ZK proofs to make transaction on chain private and untraceable.

The rest of the article is going to be hypothetical and “what if we” mindset, Let us consider some specific elements and apps of Web 2.0 that can make use of Zero Knowledge proof. 
 
1. Trust and Authentication 
2. Protecting personal and sensitive information from the verifier, third parties and other users of the service

## Trust and Authentication 
Every year, millions of usernames and passwords are compromised. This happens when hackers exploit security flaws in the main service or compromise third party services which provide solutions for these main services. 

Think about Single-Sign ons. Google and facebook can provide all information that they got when you use their service for signing up for third party services. Sign In with Apple uses bits of Zero-Knowledge proof protocol where it creates a random private relay email ID for each sign up, thereby Apple acts as a mediator between you and the service provider as to confirm you are who you say you are without revealing any private information about you or your real email address. Even if the service gets hacked, only your random relay ID gets out and none of your personal information is lost. 

The downside is, apple acts as the centralised mediator in this information exchange therefore, if your apple account were to be compromised or you get locked out of your account, you lose access to all the services you signed up through it as your identity cannot be verified anymore. Your identity and personal information can also be compromised if your apple account were to fall into wrong hands. If you ask me, when would that happen, you might not be familiar with this [article from the verge](https://www.theverge.com/2022/3/30/23003600/apple-meta-shared-data-hackers-pretending-law-enforcement-officials) where apple and meta “mistakenly” shared private user data to hackers.

![Example journeys of SSO](https://benhur.me/img/Zkproof/SSO-journey.png)

Assuming every future services run as decentralised applications (dapps) on chain, ZK proofs can be used in this case where every service can ask you for a certain combination of information that can be verified on chain, but none are complete to be able to tell who you are. This would ensure that the information you are sharing is trusted, immutable and non fungible (unique). Of course, we need to rethink ways of issuing these personal identities on chain but that is a separate challenge itself.

For example: To sign up for a car rental agency service (app or through website), today, they ask you information like your passport and sensitive document scans to verify your identity. This can be dangerous because
1. Users don’t read the terms and conditions
2. Users care about how their sensitive data is handled but do not bother reading extensive pages of information
3. The service can go out of business and hold sensitive data (Not all countries are under GDPR)
4. The service can get hacked which might result in identity theft
5. The service can provide user data to hackers disguising as law

ZK proof can be used by you, the user (prover) to the rental agency (verifier) that you are indeed 18 years old without sharing your whole passport and birth certificates which could have information about your family, address etc. Instead, you could just share a QR code or a public chain address that hosts unique key information like your birth year, name and post-code with valid government stamping that is encrypted by hash that only a few authorised keys can access. Providing this key minimal information is enough for a service provider to allow you to use the platform and get your car delivered to you. Remember even if the service provider gets exploited and user data gets hacked, your personal identifiable information never left you.

![How a possible example journey might look with Zk proof ](https://benhur.me/img/Zkproof/Good-journey.png)

Upon car-delivery, you could be asked to verify who you are which brings us to our second objective of ZK proof that is, if you can match the information on the blockchain.

## Protecting personal and sensitive information from the verifier, third parties and other users of the service
In case you were wondering, the problem was already solved. You have given a cryptographic proof that is on the blockchain. In this case when you are asked to prove your identity, all you have to do is show your physical copy / pdf of the **complete certificate** that the agency can verify if they are the same without getting a copy in their hands and you are good to go. This means that, the service provider does not possess any information or data about you but has still verified that you can be trusted with their cars. 

If you got the time, I recommend you read this article on how an [Indian state government used Polygon blockchain to issue verifiable certificates](https://cointelegraph.com/news/indian-state-gov-t-uses-polygon-to-issue-verifiable-caste-certificates)

Although discovered in the 80s, ZK proof use cases in technology are just being explored and they are slowly being rolled out in finance and government products. Learning and gaining knowledge about these new verification protocols will allow us designers, to create new products that are more privacy and user friendly while respecting the value of personal user data. Instead of just asking for passports and important documents, let’s us think about how can use these new technologies and protocols to help us create the next generation of products that don’t fall into the same trap of Web 2.0.
 
*** 
