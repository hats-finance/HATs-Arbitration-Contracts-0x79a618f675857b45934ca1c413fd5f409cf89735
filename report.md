# **HATs Arbitration Contracts Audit Competition on Hats.finance** 


## Introduction to Hats.finance


Hats.finance builds autonomous security infrastructure for integration with major DeFi protocols to secure users' assets. 
It aims to be the decentralized choice for Web3 security, offering proactive security mechanisms like decentralized audit competitions and bug bounties. 
The protocol facilitates audit competitions to quickly secure smart contracts by having auditors compete, thereby reducing auditing costs and accelerating submissions. 
This aligns with their mission of fostering a robust, secure, and scalable Web3 ecosystem through decentralized security solutions​.

## About Hats Audit Competition


Hats Audit Competitions offer a unique and decentralized approach to enhancing the security of web3 projects. Leveraging the large collective expertise of hundreds of skilled auditors, these competitions foster a proactive bug hunting environment to fortify projects before their launch. Unlike traditional security assessments, Hats Audit Competitions operate on a time-based and results-driven model, ensuring that only successful auditors are rewarded for their contributions. This pay-for-results ethos not only allocates budgets more efficiently by paying exclusively for identified vulnerabilities but also retains funds if no issues are discovered. With a streamlined evaluation process, Hats prioritizes quality over quantity by rewarding the first submitter of a vulnerability, thus eliminating duplicate efforts and attracting top talent in web3 auditing. The process embodies Hats Finance's commitment to reducing fees, maintaining project control, and promoting high-quality security assessments, setting a new standard for decentralized security in the web3 space​​.

## HATs Arbitration Contracts Overview

We turn black hat hackers into white hat hackers using the right incentives. Creating the future of security on _EVM

## Competition Details


- Type: A public audit competition hosted by HATs Arbitration Contracts
- Duration: 2 weeks
- Maximum Reward: $28,000
- Submissions: 74
- Total Payout: $24,900.4 distributed among 8 participants.

## Scope of Audit

The scope of the competition includes all the contracts that make up the HATs system, but we are specifically interested in the changes made since v2.0.

There are a number of changes since our last release:

- We added an arbitration procedure: if there is any kind of dispute about the payout, the decision can be  escalated to an Expert Committee, and if that committee cannot find consensus, to the Kleros court. The intended behavior of that system is documented here: https://github.com/hats-finance/hats-contracts/blob/audit/docs/claims.md
- The functionality of the main contract, HATVault.sol, was split into two new files (HATVault.sol and HATClaimsManager.sol) 
- We added some helper contracts, such as the PaymentSplitter.sol

The contracts that are currently in use, v2.0, can be found here https://github.com/hats-finance/hats-contracts/tree/v2.0.  


In this competition, we are interested in the usual programming errors, but we are also interested in any scenarios in which the arbitration procedure can be abused or hijacked. (For such attacks, it is the behavior that is implemented that serves as a reference - pointing out mistakes in documentation is appreciated, but will not be rewarded). 





## Low severity issues


- **Deprecated Transfer Function Causes Transaction Failures in Smart Contracts**

  The issue relates to the transfer() and send() functions in Ethereum, which forward a fixed amount of 2300 gas. It has been noted that during hard forks, the gas costs of EVM instructions might change significantly and break contract systems that make assumptions about fixed gas costs, resulting in failed transactions. A suggested fix has been provided to avoid using these functions and instead use a method that checks that the send operation was successful.


  **Link**: [Issue #25](https://github.com/hats-finance/HATs-Arbitration-Contracts-0x79a618f675857b45934ca1c413fd5f409cf89735/issues/25)



## Conclusion

The audit report of Hats.finance's Arbitration Contracts audit competition reveals the proactive security measures applied to secure users' assets. This innovative mechanism offers a decentralized approach towards enhancing the security of web3 projects, attracting and rewarding top auditing talent to discover potential vulnerabilities before a project's launch. A bug hunting environment and time-based results-driven model incentivize auditors to identify and rectify issues efficiently. Successfully tested during a two-week public audit competition, a total of $24,900.4 was distributed among eight participants. Importantly, several programming issues and potential vulnerabilities for abuse or hijacking of the arbitration procedure were identified. The process further exemplifies Hats' commitment to high-quality, cost-efficient, decentralized auditing while also attracting top talent, setting new security standards in the web3 space.

## Disclaimer


This report does not assert that the audited contracts are completely secure. Continuous review and comprehensive testing are advised before deploying critical smart contracts./n/n
The HATs Arbitration Contracts audit competition illustrates the collaborative effort in identifying and rectifying potential vulnerabilities, enhancing the overall security and functionality of the platform.


Hats.finance does not provide any guarantee or warranty regarding the security of this project. All smart contract software should be used at the sole risk and responsibility of users.

