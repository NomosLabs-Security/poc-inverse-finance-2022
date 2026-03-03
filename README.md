# Inverse Finance Keep3r TWAP Oracle Manipulation — PoC

> **Educational Purpose Only** — This PoC is created for security research and education
> purposes only. It runs against a fork, not mainnet.

## Quick Start

```bash
git clone https://github.com/NomosLabs-Security/poc-inverse-finance-2022
cd poc-inverse-finance-2022
forge install foundry-rs/forge-std --no-git
forge test -vvvv
```

## Details

- **Exploit Date:** 2022-04-02
- **Fork Block:** #14506359
- **Expected Output:** TWAP oracle manipulation via sustained buying on low-liquidity SushiSwap pair
- **Full Analysis:** [NomosLabs Security Intelligence Archive](https://nomoslabs.io/archive/inverse-finance-2022)

## Description

Inverse Finance's Anchor protocol used a Keep3r TWAP oracle reading from the
SushiSwap INV/ETH pair (~$3.5M liquidity). The attacker manipulated the TWAP
over ~30 minutes of sustained buying, inflating INV collateral value, then
borrowed $15.6M in DOLA and ETH against the overvalued collateral.

## License

MIT — For educational use only.
