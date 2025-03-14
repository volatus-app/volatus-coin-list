# Volatus Coin List

This repository contains the token list used by the Volatus Swap Aggregator.

## What are token lists?
Volatus Token Lists is a specification for lists of token metadata (e.g. address, decimals, ...) that can be used by any dApp interfaces that need one or more lists of tokens.

Specifically an instance of a token list is a JSON blob that contains a list of ERC20 token metadata for use in dApp user interfaces. Token list JSON must validate against the JSON schema in order to be used in the Volatus Interface. Tokens on token lists, and token lists themselves, are tagged so that users can easily find tokens.

## Usage

You can access the token list directly from GitHub:

```javascript
// Example of fetching the token list
async function getTokenList() {
  const response = await fetch('https://raw.githubusercontent.com/volatus-app/volatus-coin-list/main/volatus-coins.json');
  const tokenList = await response.json();
  return tokenList;
}
```

## Token Information

Each token in the list includes:
- Contract address
- Name
- Symbol
- Decimal precision
- Logo image URL