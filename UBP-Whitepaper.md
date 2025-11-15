# UBP — Universal Blockchain Protocol
Version: 1.0
Author: Kram

## 1. Introduction
Blockchains today use different formats for addresses, transactions, tokens, and explorers. This creates confusion, increases user mistakes, and makes cross-chain development harder.

UBP solves this problem with a simple, universal, human-readable link standard that works for any blockchain.

## 2. What is UBP?
UBP is a unified link notation:

ubp:<chain>/<type>/<value>

Examples:
ubp:btc/tx/111aaa
ubp:eth/address/0xABCDEF123
ubp:sol/token/So111111111111111111

UBP defines:
- a universal prefix (ubp:)
- a chain identifier (sol, eth, btc, etc.)
- a type (address, tx, token, nft, contract)
- a value (the chain-specific data)

## 3. Why UBP Matters
### 3.1 Cross-chain simplicity
One standard for all blockchains removes dozens of incompatible link formats.

### 3.2 Fewer user mistakes
Users instantly see the chain and type. Wallets and explorers can auto-detect and route correctly.

### 3.3 Copy-paste friendly
A single readable format works across apps, tools, wallets, and explorers.

## 4. Technical Overview (V1 Summary)
UBP supports:
- Chains: btc, eth, sol, ton, bnb, matic, etc.
- Types: address, tx, token, nft, contract
- Extensions: future-proof fields like /memo or /network

Validation: each chain validates its own format. UBP only standardizes structure.

Resolvers: tools that convert UBP links into real explorer URLs.
Example:
ubp:sol/address/9xKram → https://solscan.io/address/9xKram

Resolvers can be:
- browser extensions
- wallet integrations
- explorer integrations
- backend APIs

## 5. Benefits
### For Users:
- No confusion between chains
- Avoid incorrect chain transactions
- Easier sharing

### For Developers:
- One standard for all identifiers
- Simple parsing rules
- Cleaner cross-chain compatibility

### For the Ecosystem:
- Improves interoperability
- Reduces fragmentation
- Enables multi-chain tools

## 6. Use Cases
- Multi-chain wallets
- Token explorers
- NFT verification
- Messaging apps
- Payment systems
- Analytics dashboards
- Cross-chain identity systems

## 7. Roadmap (Short)
- V1 launch
- Resolver browser extension + API
- Community registry for chains/types
- Integration partnerships
- V2 with advanced metadata features

## 8. Conclusion
UBP unifies blockchain identifiers using a simple, readable, and open format. It reduces mistakes, increases interoperability, and makes blockchain tools easier to build and use.

UBP is open-source, chain-agnostic, and designed for adoption by wallets, explorers, developers, and users worldwide.
