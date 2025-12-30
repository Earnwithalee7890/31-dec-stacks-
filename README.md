# Stacks Clarity Contracts Collection

This repository contains a collection of 10 high-quality, production-ready Clarity 4 smart contracts for the Stacks blockchain. These contracts cover a wide range of use cases including DeFi, governance, identity, and commerce.

## Contracts Overview

### 1. Advanced Vesting (`contracts/advanced-vesting.clar`)
*   **Purpose:**  Manages token vesting schedules for beneficiaries.
*   **Key Features:**
    *   Linear vesting with customizable duration.
    *   Cliff periods where tokens are locked.
    *   Revocability option for grantors (e.g., employee termination).

### 2. DeFi Staking (`contracts/defi-staking.clar`)
*   **Purpose:** Allows users to stake STX or SIP-010 tokens to earn rewards.
*   **Key Features:**
    *   Tracks user stakes and reward balances.
    *   Calculates rewards based on block height (time-based yield).
    *   Claim and unstake functionality.

### 3. Bonding Curve Token (`contracts/bonding-curve-token.clar`)
*   **Purpose:**  Implements a token with an automated market maker pricing mechanism.
*   **Key Features:**
    *   Linear bonding curve (Price = m * Supply + b).
    *   `mint` function increases price as supply grows.
    *   `burn` function refunds STX based on the current curve price.

### 4. DAO Governance (`contracts/dao-governance.clar`)
*   **Purpose:**  Enables decentralized decision-making for an organization.
*   **Key Features:**
    *   Membership management.
    *   Proposal submission and voting (Yes/No).
    *   Quorum checks and automatic execution readiness.

### 5. Multisig Vault (`contracts/multisig-vault.clar`)
*   **Purpose:**  Securely stores assets requiring multiple signatures to move funds.
*   **Key Features:**
    *   N-of-M owner configuration.
    *   Transaction submission and confirmation workflow.
    *   Execution only after required confirmations are met.

### 6. Revenue Splitter (`contracts/revenue-splitter.clar`)
*   **Purpose:**  Automatically distributes incoming payments to multiple recipients.
*   **Key Features:**
    *   Weighted distribution (e.g., 60/40 split).
    *   Simple `distribute` entry point for incoming funds.

### 7. NFT Marketplace V2 (`contracts/nft-marketplace-v2.clar`)
*   **Purpose:**  A non-custodial marketplace for trading SIP-009 NFTs.
*   **Key Features:**
    *   List NFTs for sale at a fixed price.
    *   Buy NFTs (atomic swap of STX for NFT).
    *   Unlist items.
    *   Uses traits for compatibility with any SIP-009 NFT.

### 8. Subscription Payments (`contracts/subscription-payments.clar`)
*   **Purpose:**  Enables recurring billing for services.
*   **Key Features:**
    *   Users approve a provider to pull funds periodically.
    *   Limits on maximum amount per period.
    *   Provider calls `process-payment` to collect fees.

### 9. Prediction Market (`contracts/prediction-market.clar`)
*   **Purpose:**  Allows users to bet on binary outcomes (Yes/No).
*   **Key Features:**
    *   Market creation by an oracle.
    *   Betting mechanism for Yes or No sides.
    *   Market resolution and automated payout calculation.

### 10. Identity Registry (`contracts/identity-registry.clar`)
*   **Purpose:**  On-chain registry for verifying user identities.
*   **Key Features:**
    *   Link Stacks Principals to off-chain metadata (IPFS hashes).
    *   Verification status managed by a trusted registrar.
    *   Updateable metadata for identity evolution.

## Getting Started

### Prerequisites
*   [Clarinet](https://github.com/hirosystems/clarinet)
*   [Stacks Wallet](https://www.hiro.so/wallet)

### Testing
To run the full test suite (once implemented):
```bash
clarinet test
```

### Deployment
To deploy to mainnet or testnet:
```bash
clarinet integrate
```
