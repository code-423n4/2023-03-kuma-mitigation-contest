# KUMA Protocol - Mitigation contest details
- Total Prize Pool: $11,000 USDC 
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-Versus-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Submit findings [using the C4 form](https://code4rena.com/contests/2023-03-kuma-protocol-mitigation-contest/submit)
- Starts March 16, 2023 20:00 UTC
- Ends March 21, 2023 20:00 UTC

## Important note 

Each warden must submit a mitigation review for *every High and Medium finding* from the parent contest. **Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

- [H-01: TRANSFERING KIBToken TO YOURSELF INCREASES YOUR BALANCE](https://github.com/code-423n4/2023-02-kuma-findings/issues/3)
- [M-01: KUMABondToken.approve() should revert if the owner of the tokenId is blacklisted](https://github.com/code-423n4/2023-02-kuma-findings/issues/22)
- [M-02: KUMAFeeCollector.changePayees() executes incorrectly when newPayees contains duplicate items ](https://github.com/code-423n4/2023-02-kuma-findings/issues/13)
- [M-03: Price feed in MCAGRateFeed#getRate is not sufficiently validated and can return stale price](https://github.com/code-423n4/2023-02-kuma-findings/issues/11)
- [M-04: KUMASwap incorrectly reverts when when _maxCoupons has been reached](https://github.com/code-423n4/2023-02-kuma-findings/issues/10)

## Overview of changes

Please provide context about the mitigations that were applied if applicable and identify any areas of specific concern.

## Mitigations to be reviewed

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo. 

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| https://github.com/code4rena/sample-contracts/pull/XXX | H-01 | This mitigation does XYZ | 

## Out of Scope

Please list any High and Medium issues that were judged as valid but you have chosen not to fix.
