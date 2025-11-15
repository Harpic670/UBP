# UBP Resolver — Concept Overview

A UBP Resolver is a tool or service that converts UBP links into real blockchain explorer URLs.

Example:
UBP → Explorer URL

ubp:btc/tx/abcd1234
→ https://mempool.space/tx/abcd1234

ubp:sol/address/9xKram1111
→ https://solscan.io/address/9xKram1111

ubp:eth/contract/0xABC123
→ https://etherscan.io/address/0xABC123

## Why This Matters
Without a resolver, UBP is just a string format.
With a resolver, UBP becomes a practical standard that apps, wallets, and explorers can support.

## How a Basic Resolver Works
A resolver takes three inputs:
- chain
- category
- identifier

Then maps them to:
- a known blockchain explorer
- the correct URL format

## Example Mapping Table

| Chain | Category | Explorer Base URL |
|-------|----------|------------------|
| btc | tx | https://mempool.space/tx/ |
| eth | tx | https://etherscan.io/tx/ |
| eth | address | https://etherscan.io/address/ |
| sol | address | https://solscan.io/address/ |
| sol | tx | https://solscan.io/tx/ |
| sol | token | https://solscan.io/token/ |

## Example Pseudocode (Resolver Logic)

function resolveUBP(ubpString):
    parts = ubpString.split("/")
    base = parts[0]           # ubp:btc
    chain = base.replace("ubp:", "")
    category = parts[1]
    value = parts[2]

    lookup explorer URL from mapping table
    return explorerURL + value

## Future Resolver Ideas
- Browser extension that auto-detects UBP
- Wallets opening UBP links directly
- Universal QR codes
