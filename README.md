# h3-Hashes

## Protocol Building Blocks

- A protocol is a series of steps, involving two or more parties, designed to accomplish a task.
- One person alone doesn't make a protocol, but it always reguires at least two perosns to complete the protocol.
- One person can perform a series of steps to accomplish a task but it is not a protocol.

- A cryptographic protocol is a protocol that uses cryptography.
- The whole point of using cryptography in a protocol is to prevent or detect cheating and wiretapping.
- It should be impossible to exceed or acquire knowledge beyond the defined parameters outlined in the protocol.

- These days communication is done more and more through computer instead of face to face.
- That is why computers need formal protocols for doing same kinds of things that people do without thinking.
- No one should never trust that people on computer networks are honest. Most of them are, but few are not and that's why they can cause damage
- By formalizing protocols, we can examine ways in which dishonest parties can subvert them.
- The protocols can develop to be immune to that subversion.

- Arbitrated Protocols are distinterested third party trusted to complete the protocol.
- Arbitrators can help to complete protocols between parties that are mutually distrustful.
- The concept of an arbitrator is as old as a society, because there have been always people who have the athority to act fairly (priests, rulers). They have a certain
  social role and position in the society.

- In the computer world have several problems with computer arbitrators:
    - It is easier to find a trusted third party arbitrator, if you know who the party is
    - The computer network has to cover the expenses of keeping an arbitrator.
    - There is a natural delay
    - Every transaction must be dealed by the arbitrator; It slows down big implementations of any protocol. Adding more arbitrators can help fix this issue,
      but it also makes things more expensive.
    - Because everyone on the network has to trust the arbitrator, he becomes a weak spot for anyone attempting to undermine the network.

- Arbitrated protocols can be subdivided into two lower-level subprotocols because hiring arbitrators would be very costly.
- There are two parts to this process. First, there's a routine part that happens every time parties want to finish the protocol, and it doesn't involve arbitration.   The second part is an arbitration process, which only occurs when there's a dispute. This specific kind of arbitrator is called an adjudicator.
- An adjucator is trusted and disinterested third party and unlike an arbtrator, he is not involved directly in every protocol.

- Difference between adjudicator and arbitrator is that there is no need for adjudicator always. If there is not a dispute, there is not need for a judge.

- The best protocol is a Self-enforcing protocol.
- The protocol itself guarantees fairness
- There is no need for arbitrator to complete the protocol or adjudicator for resolvel the disputes.
- In a best world, all the protocols would be self-enforcing
- However, that is not possible in every situation.

- Attacks against protocols can be passive or active attacks
- Passive attackers are trying to gain information about the parties who are involved in the protocol.
- Active attackers are much more diverse, because they can be interested degraiding system performance, obtaining information, corrupting existing information or gaining unauthorized access to resources.

- Communication using symmetric gryptography:
    - A good cryptosystem is one in which all the security is naturally in knowledge of the key and none is naturally in knowledge of the algorithm
- That is why key management is so important in cryptgraphy.

Symmetric cryptsystems have a few problems:
  - Keys must be distributed in secret.
  - If a key is compromised Somebody can decrypt all message traffic encrypted with that key. She can also pretend to be one of the parties and produce false              messages to fool the other party.
  - The total number of keys increases rapidly as the number of users increases, if separate key is used for each pair of users in a network.
  - The concept of a one-way function is crucial in public-key cryptography. Although not protocols on their own, one-way functions serve as a fundamental building        block.
  - A trapdoor one-way function is a unique kind of one-way function that comes with a secret trapdoor. It's easy to calculate in one direction but challenging in the     opposite direction. 

## Hashcat

x) The first time I was able to do everything else in the cracking password test, except actually cracking the password in the end ;) This was maybe because there was a warning and I did not pass further, I just copy-paste the key again without any warning, and it gave me this result. 

![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/e3cf2a78-771a-4546-bd48-48f2ec47cf04)


The second time I was actually able to crack the password.
![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/328ee550-fea2-4a06-8750-7ac1a7a17bc0)
![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/d1367bad-b6d7-49d0-a0de-b8f85a4bc3b9)


a) 
voluntary bonus: Classic Bitcoin uses the SHA256 hash algorithm. SHA256 = Secure Hash Algorithms 256 Bits
https://yukimotopress.github.io/programming-blockchains-step-by-step

(I haven't been able to solve the small screen problem as I don't have the "Devices" in my menu bar. I tried to look around the web but it seems, that others have had the same problem and solving it is not easy.)
https://forums.virtualbox.org/viewtopic.php?t=108844, https://forums.virtualbox.org/viewtopic.php?t=77473
https://superuser.com/questions/893159/cant-install-guest-additions-missing-devices-menu-on-host
Sometimes I also must boot the virtual box as it gets stucked.)

- b) Compare hash. Create a small text file. Take it's hash (e.g. 'sha256sum tero.txt'). Change one letter. Take the hash again. Compare hashes. What do you notice?
      - I made a new file, but I don't understand where I can take it's hash? I just can't realize what I should do..
- b) Install hashcat and test that it works.
- c) Crack this hash: 21232f297a57a5a743894a0e4a801fc3

I was able to identify the hash  type
![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/e0247ad0-0214-4417-b239-4c68d5dcace3)

Then I tryed to crack the password, but I realized that I need to add the dictionary. 

![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/31a2b7de-899d-4fb3-8b63-71543e2f86ba)

Then I got the dictionary rockyou.txt

![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/b4e5c52d-77ef-4fb5-b788-333f4a8e2273)

Then I cracked the password:

![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/e5a08342-c2e6-4df0-b5ed-99dc58126de8)

But then I lost it...

I tryed to find it..

![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/fcfcc866-7653-4899-84a1-09d8c1f655b1)

But I am not sure is the password: admin

- d) Crack this Windows NTLM hash: f2477a144dff4f216ab81f2ac3e3207d

It started doing a lot of things when I put "hashcat -m 0  f2477a144dff4f216ab81f2ac3e3207d

And ended up like this

![image](https://github.com/Eeva1/h3-Hashes/assets/149093822/be458216-29a8-4593-82bb-2e7f10a9478f)

This page is interesting

- e) Try cracking this hash and comment on your hash rate $2y$18$axMtQ4N8j/NQVItQJed9uORfsUK667RAWfycwFMtDBD6zAo1Se2eu . This subtask d does not require actually cracking the hash, just trying it and commenting on the hash rate.



 





      
