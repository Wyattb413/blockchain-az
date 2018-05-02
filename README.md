# Build Your Own Blockchain A-Z Notes

[**Udemy Course Link**](https://www.udemy.com/build-your-blockchain-az/learn/v4/content) - https://www.udemy.com/build-your-blockchain-az/learn/v4/content

## Table of Contents

Lecture Topic | Link
--- | ---
**SECTION 3** | [**Section 3**](#section-3)
What is a Blockchain | [Lecture 6](#section-3-lecture-6)
What is a BlockchainUnderstanding SHA256 - Hash | [Lecture 7](#section-3-lecture-7)
The Immutable Ledger | [Lecture 8](#section-3-lecture-8)
Distrubuted P2P Network | [Lecture 9](#section-3-lecture-9)

<!-- ################################################################################################################ -->
<!--                                                     SECTION 3                                                    -->
<!-- ################################################################################################################ -->

## SECTION 3

### Section 3 Lecture 6

#### What is a Block Chain

[**How to Time Stamp a Digital Document**](https://www.anf.es/pdf/Haber_Stornetta.pdf) - Stuart Haber & W. Scott Stornetta, (1991)

- **Stuart Haber** and **W. Scott Stornetta** created the foundation behind the blockchain "How to Time-Stamp a Digital Document"
- **Blockchain**: A blockchain is a continuously growing list of records, called blocks, which are linked and secured using cryptography (Wikipedia)
- **Blocks** contain Data, Previous Hash, and Hash (a finger print of the **Data** and the **Previous Hash**)
- **Genesis Block** is the first block in a blockchain
- The **Hash** generated for each **Block** is a cryptographic signature of the **Previous Hash** and the **Data** contained within the **Block**. This insures security of the entire chain by providing a cryptographic method of checking whether a block's **Data** has been tampered with after being added to the **Block Chain**

### Section 3 Lecture 7

#### Understanding SHA256 - Hash

[**On the Secure Hash Algorithm family (Chapter 1 of Cryptography in Context)**](https://www.staff.science.uu.nl/~tel00101/liter/Books/CrypCont.pdf)

[**Live SHA256 Demo**](https://tools.superdatascience.com/blockchain/hash)

- **SHA256 Hash**ing algorithm was developed by the NSA
- **SHA** Secure Hashing Algorithm
- **256** represents the number of bits it takes up in memory
- **64** characters long
- **Hexidecimal** hash, contains 0-9 a-f

##### 5 requirements for Hash algorithms

- **One way** unable to restore the **Data** from the **Hash**
- **Deterministic** every-time the same **Data** is hashed, the same **Hash** is **ALWAYS** generated
- **Fast Computation**
- **The Avalanche Effect** any changes the is made to the **Data** will result in a completely different **Hash** being generated
- **Must withstand collisions** the algorithm needs to be able to withstand artificial collisions

### Section 3 Lecture 8

#### The Immutable Ledger

[**The Blockchain Economy: A beginner's guide to institutional cryptoeconomics** - Chris Berg, Sinclair Davidson & Jason Potts (2017)](https://medium.com/@cryptoeconomics/the-blockchain-economy-a-beginners-guide-to-institutional-cryptoeconomics-64bf2f2beec4)

Each _transaction_ that's recorded in the **Ledger** gets a cryptographic **Hash** generated from it's **Data**; This **Hash** is used when linking to the next _transaction_. Because of the nature of **Hash**es, if any entity attempted to alter the **Data** in any _transaction_, the resulting **Hash** would change, invalidating the the **Ledger** from there on. As more _transactions__ are added to the **Ledger** rectifying the altered **Ledger** becomes increasingly difficult, as every **Hash** after the altered _transaction_ will have to be updated to accept each updated **Hash**.

### Section 3 Lecture 9

#### Distributed P2P Network

In simple terms, a **Peer-to-Peer (P2P) network** is dividing the hosts of a network amongst several "mini-servers" (a.k.a. **Peers**) instead of a few main-servers.

So, instead of all users connecting to _Server A_ and reading / writing their data there, users of the network can connect to one of several **Peers** and read / write from there.

Alternatively, users can become a **Peer** themselves, and host their own copy of the network.

A couple of **benefits** of a **P2P Network** are:

- **Higher probability of uptime**: Because there can be multiple copies of network hosted by several **Peers**, if one or a couple of **Peers** would to go offline, users could still access the network by connecting to **Peers** whom are still online. On the contrary, if all users of the network connected solely to _Server A_, if _Server A_ were to be taken offline, all users loose access to the network
- **Cheaper**: By having your network spread across many "mini-servers", you promote the ability of dividing network traffic. Instead of needing a beefy server that could handle thousands of requests per second, you could alternatively have ten smaller servers (**Peers**) handling hundreds of requests per second

A couple of **disadvantages** of a **P2P Network** are:

- **Isolated Unreliability**: Because a **Peer** can be anyone, the chances that a specific mini-server (**Peer**) could go offline is completely dependant on the owner of the mini-server. This by itself isn't exactly a glaring problem, but for example, let's say you were in the middle of streaming files from a specific **Peer** and they went offline

![Distributed P2P Network Diagram](img/p2p-diagram.png?raw=true "Distributed P2P Network Diagram")

In the above example, each laptop represents a **Peer** in the particular network. Each **Peer** is storing and managing their own version of the **Blockchain**.