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

-  Arbitrated protocols can be subdivided into two lower-level subprotocols because hiring arbitrators would be very costly.
-  There are two parts to this process. First, there's a routine part that happens every time parties want to finish the protocol, and it doesn't involve arbitration. The second part is an arbitration process, which only occurs when there's a dispute. This specific kind of arbitrator is called an adjudicator.
      
