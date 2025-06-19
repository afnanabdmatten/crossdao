---

# crossdao

A decentralized autonomous organization (DAO) smart contract built with [Clarity](https://docs.stacks.co/write-smart-contracts/clarity-language) for the Stacks blockchain. This contract implements staking, proposal submission, voting, and reward distribution using a custom fungible token (`xSTX`).

## Features

- **SIP-010 Fungible Token**: Implements the `xSTX` token.
- **Staking**: Users can stake STX to mint `xSTX`.
- **Governance**: Submit proposals, vote, and execute proposals.
- **Rewards**: Distribute and claim staking rewards.
- **Emergency Controls**: Emergency exit and contract controls.


### Prerequisites

- [Clarinet](https://docs.hiro.so/clarinet/get-started) (for local development and testing)
- [Node.js](https://nodejs.org/) (for running tests)

### Build & Test

```sh
clarinet check
clarinet test
npm install
npm test
```

## Contract Overview

- **Staking**:  
  `stake-stx(amount)` — Stake STX and receive `xSTX`.
- **Proposals**:  
  `submit-proposal(description, duration)` — Submit a new proposal.  
  `vote(id, support)` — Vote for or against a proposal.  
  `execute-proposal(id)` — Execute a proposal if it passes.
- **Rewards**:  
  `claim-rewards()` — Claim accumulated rewards.  
  `distribute-rewards()` — Distribute rewards to stakers.
- **Emergency**:  
  `trigger-emergency()` — Only contract owner can trigger.  
  `exit-stake()` — Emergency withdrawal for stakers.

