# Build Your Own Blockchain A-Z Notes

[**Udemy Course Link**](https://www.udemy.com/build-your-blockchain-az/learn/v4/content) - https://www.udemy.com/build-your-blockchain-az/learn/v4/content

## Table of Contents

Lecture Topic | Link
--- | ---
**SECTION 3** | [**Section 3**](#section-3)
What is a Blockchain | [Lecture 6](#section-3-lecture-6)
What is a BlockchainUnderstanding SHA256 - Hash | [Lecture 7](#section-3-lecture-7)
The Immutable Ledger | [Lecture 8](#section-3-lecture-8)

<!-- ################################################################################################################ -->
<!--                                                     SECTION 3                                                    -->
<!-- ################################################################################################################ -->

## SECTION 3

### Section 3 Lecture 6

#### What is a Block Chain

[**How to Time Stamp a Digital Document**](https://www.anf.es/pdf/Haber_Stornetta.pdf) - Stuart Haber & W. Scott Stornetta, (1991)

- **Stuart Haber** and **W. Scott Stornetta** created the foudation behind the blockchain "How to Time-Stamp a Digital Document"
- **Blockchain**: A blockchain is a continuously growing list of records, called block, which are linked and secured using cryptography (Wikipedia)
- **Blocks** contain Data, Previous Hash, and Hash (a finger print of the **Data** and the **Previous Hash**)
- **Genesis Block** is the first block in a blockchain
- The **Hash** generated for each **Block** is a cryptographic signature of the **Previous Hash** and the **Data** contained within the **Block**. This insures security of the entire chain by providing a cryptographic method of checking whether a block's **Data** has been tampered with after being added to the **Block Chain**

### Section 3 Lecture 7

#### Understanding SHA256 - Hash

[**On the Secure Hash Algorithm family (Chapter 1 of Cryptography in Context)**](https://www.staff.science.uu.nl/~tel00101/liter/Books/CrypCont.pdf)

- **SHA256 Hash**ing algorithm was developed by the NSA
- **SHA** Secure Hasing Algorithm
- **256** represents the number of bits it takes up in memory
- **64** characters long
- **Hexidecimal** hash, contains 0-9 a-f

##### 5 requirements for Hash algorithms

- **One way** unable to restore the **Data** from the **Hash**
- **Deterministic** everytime the same **Data** is hashed, the same **Hash** is **ALWAYS** generated
- **Fast Computation**
- **The Avalanche Effect** any changes the is made to the **Data** will result in a completely different **Hash** being generated
- **Must withstand collisions** the algorithm needs to be able to withstand artificial collisions

### Section 3 Lecture 8

#### The Immutable Ledger

[**The Blockchain Economy: A beginner's guide to institutional cryptoeconomics** - Chris Berg, Sinclair Davidson & Jason Potts (2017)](https://medium.com/@cryptoeconomics/the-blockchain-economy-a-beginners-guide-to-institutional-cryptoeconomics-64bf2f2beec4)

Each _transaction_ that's recorded in the **Ledger** get's a cryptographic **Hash** generated from it's **Data**; This **Hash** is used when linking to the next _transaction_. Because of the nature of **Hash**es, if any entitiy attempted to alter the **Data** in any _transaction_, the resulting **Hash** would change, invalidating the the **Ledger** from there on. As more _transactions__ are added to the **Ledger** recitifying the altered **Ledger** becomes increasingly difficult, as every **Hash** after the altered _transaction_ will have to be updated to accept each updated **Hash**.