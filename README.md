# Legacy notice

This repository describes NVX, an earlier token project. It is **not** the live official NOVARIC® token.

The live official token is **NVRCX**, a BEP-20 token on BNB Smart Chain.

- Contract: `0x5f95c93DF927FB5C16be333f2E398FA77BdFb2f8`
- Official page: https://novaric.eu/en/nvrcx/
- Whitepaper (v1.1): https://novaric.eu/en/nvrcx/assets/NVRCX-Whitepaper-v1.1-20261118.pdf
- BscScan: https://bscscan.com/token/0x5f95c93DF927FB5C16be333f2E398FA77BdFb2f8
- Official X: https://x.com/novaric_europe
- Official Telegram announcements: https://t.me/novaric_nvrcx
- Reports: security@novaric.co

NOVARIC® never DMs first and never asks for a seed phrase or private key.

On-chain name / symbol: NOVARIC® / NVRCX. The contract records the name as NOVARIC, without the ®. Decimals: 18. Total supply: 10,000,000,000 NVRCX (fixed cap). Ownership is held by a 2-of-3 Safe at `0xd0CDd8C780571B24C77DA8bE7B26B5d799cCAA97`. The only liquidity pool identified for NVRCX is the PancakeSwap V2 NVRCX/WBNB pair at `0xe9d0EDFF80150AA74270639b30EaCcD0d7Ba0Ea6`. Current amounts and lock records are on the official page.

Do not use any contract address from the files below, or from older materials, unless it matches the official page exactly (all 40 hex characters). Contracts named in earlier NOVARIC® materials, including `0xfF6bAeD9D98E8eD07f5Aa0B36C3d7a469fa5BF5e`, `0xcb4B65065f9a3146FF7F5af18f4B0E4012f807F6`, `0x39E4d2285bC51a12588341213A05E523C928bF46` and `0xcB76E0ca127dC08168bCcEEC958F02Fa9fda1e91`, are not the live official token.

The files below are retained for history. They are not a current token specification and they are not an invitation to trade.

---

<!-- Keep the existing Trust Wallet Assets README below this line, unchanged. -->

# Trust Wallet Assets Info

![Check](https://github.com/trustwallet/assets/workflows/Check/badge.svg)

## Overview

Trust Wallet token repository is a comprehensive, up-to-date collection of information about several thousands (!) of crypto tokens.

[Trust Wallet](https://trustwallet.com) uses token logos from this source, alongside a number of other projects.

The repository contains token info from several blockchains, info on dApps, staking validators, etc.
For every token a logo and optional additional information is available (such data is not available on-chain).

Such a large collection can be maintained only through a community effort, so _feel free to add your token_.

<center><img src='https://trustwallet.com/assets/images/media/assets/horizontal_blue.png' height="200"></center>

## How to add token

Please note that __brand new tokens are not accepted__,
the projects have to be sound, with information available, and __non-minimal circulation__
(for limit details see <https://developer.trustwallet.com/listing-new-assets/requirements>).

### Assets App

The [Assets web app](https://assets.trustwallet.com) can be used for most new token additions (Github account is needed).

### Quick starter

Details of the repository structure and contribution guidelines are listed on the
[Developers site](https://developer.trustwallet.com/listing-new-assets/new-asset).
Here is a quick starter summary for the most common use case.


## Documentation

For details, see the [Developers site](https://developer.trustwallet.com):

- [Contribution guidelines](https://developer.trustwallet.com/listing-new-assets/repository_details)

- [FAQ](https://developer.trustwallet.com/listing-new-assets/faq)

## Scripts

There are several scripts available for maintainers:

- `make check` -- Execute validation checks; also used in continuous integration.
- `make fix` -- Perform automatic fixes where possible
- `make update-auto` -- Run automatic updates from external sources, executed regularly (GitHub action)
- `make add-token asset_id=c60_t0x4Fabb145d64652a948d72533023f6E7A623C7C53` -- Create `info.json` file as asset template.
- `make add-tokenlist asset_id=c60_t0x4Fabb145d64652a948d72533023f6E7A623C7C53` -- Adds a token to tokenlist.json.
- `make add-tokenlist-extended asset_id=c60_t0x4Fabb145d64652a948d72533023f6E7A623C7C53` -- Adds a token to tokenlist-extended.json.

## On Checks

This repo contains a set of scripts for verification of all the information. Implemented as Golang scripts, available through `make check`, and executed in CI build; checks the whole repo.
There are similar check logic implemented:

- in assets-management app; for checking changed token files in PRs, or when creating a PR.  Checks diffs, can be run from browser environment.
- in merge-fee-bot, which runs as a GitHub app shows result in PR comment. Executes in a non-browser environment.

## Trading pair maintenance

Info on supported trading pairs are stored in `tokenlist.json` files.
Trading pairs can be updated --
from Uniswap/Ethereum and PancakeSwap/Smartchain -- using update script (and checking in changes).
Minimal limit values for trading pair inclusion are set in the [config file](https://github.com/trustwallet/assets/blob/master/.github/assets.config.yaml).
There are also options for force-include and force-exclude in the config.

## Disclaimer

Trust Wallet team allows anyone to submit new assets to this repository. However, this does not mean that we are in direct partnership with all of the projects.

Trust Wallet team will reject projects that are deemed as scam or fraudulent after careful review.
Trust Wallet team reserves the right to change the terms of asset submissions at any time due to changing market conditions, risk of fraud, or any other factors we deem relevant.

Additionally, spam-like behavior, including but not limited to mass distribution of tokens to random addresses will result in the asset being flagged as spam and possible removal from the repository.

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
