# KUMA Protocol - Mitigation contest details

- Total Prize Pool: $11,000 USDC
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-Versus-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Submit findings [using the C4 form](https://code4rena.com/contests/2023-03-kuma-protocol-versus-mitigation-contest/submit)
- Starts March 16, 2023 20:00 UTC
- Ends March 21, 2023 20:00 UTC

## Important note

Each warden must submit a mitigation review for:

- Every High and Medium finding listed below, and
- one report each for the Gas and QA fixes.

For the Gas and QA mitigation reports:
- Write a headline for each specific finding, that indicates whether the specific finding was fixed
- Add any additional information for each finding below each headline

**Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

- [H-01: TRANSFERING KIBToken TO YOURSELF INCREASES YOUR BALANCE](https://github.com/code-423n4/2023-02-kuma-findings/issues/3)
- [M-01: KUMABondToken.approve() should revert if the owner of the tokenId is blacklisted](https://github.com/code-423n4/2023-02-kuma-findings/issues/22)
- [M-02: KUMAFeeCollector.changePayees() executes incorrectly when newPayees contains duplicate items ](https://github.com/code-423n4/2023-02-kuma-findings/issues/13)
- [M-03: Price feed in MCAGRateFeed#getRate is not sufficiently validated and can return stale price](https://github.com/code-423n4/2023-02-kuma-findings/issues/11)
- [M-04: KUMASwap incorrectly reverts when when \_maxCoupons has been reached](https://github.com/code-423n4/2023-02-kuma-findings/issues/10)
- QA Reports including [#19](https://github.com/code-423n4/2023-02-kuma-findings/issues/19), [#7](https://github.com/code-423n4/2023-02-kuma-findings/issues/7), [#23](https://github.com/code-423n4/2023-02-kuma-findings/issues/23), and [#15](https://github.com/code-423n4/2023-02-kuma-findings/issues/15).
- [Gas Report](https://github.com/code-423n4/2023-02-kuma-findings/issues/21)

## Overview of changes

This mitigation adds validation to state modifications and oracles in the KIBT, KUMASwap, MCAGRateFeed, and KUMABondToken contracts, in addition to gas optimizations and QA fixes.  


## Mitigations to be reviewed

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo.

| URL                                                  | Mitigation of | Purpose                                                                                         |
| ---------------------------------------------------- | ------------- | ----------------------------------------------------------------------------------------------- |
| https://github.com/code-423n4/2023-02-kuma/pull/3    | H-01          | This mitigation adds a check disallowing transfer to self in KIBT _transfer |
| https://github.com/code-423n4/2023-02-kuma/pull/4    | M-01          | This mitigation adds a check that the owner of a KUMABondToken approve call is not black listed |
| https://github.com/code-423n4/2023-02-kuma/pull/5    | M-02          | This mitigation adds a duplicate payees check in KUMAFeeCollector changePayees|
| https://github.com/code-423n4/2023-02-kuma/pull/6 | M-03          | This mitigation adds a staleness threshold check to MCAGRateFeed |
| https://github.com/code-423n4/2023-02-kuma/pull/7| M-04          | This mitigation fixes the logic in KUMASwap sellBond revert for when maxCoupons has been reached|
| https://github.com/code-423n4/2023-02-kuma/pull/8    | QA          | This mitigation adds QA fixes - see PR for specific fixes|
| https://github.com/code-423n4/2023-02-kuma/pull/9    | GAS          |This mitigation adds GAS fixes - see PR for specific fixes |
| https://github.com/code-423n4/2023-02-kuma/pull/10    | term-fix          |This mitigation refactors bond.term to months instead of seconds |

## Out of Scope

All high and medium issues were mitigated.
