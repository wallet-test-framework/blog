+++
title="WTF News (Week 17)"
description="And we're back, baby!"
date=2023-08-04

[taxonomies]
tags = ["Q2", "August"]
categories = ["status update"]
+++

Hello and welcome to issue number eight of WTF News, our biweekly status update.

We missed last update (sorry about that), but we're back with more tests than
ever!

<a href="./wtf-short.mp4">
    <video muted autoplay loop src="./wtf-short.mp4" style="max-width: 100%">
    <p>Demo video of an <code>eth_sendTransaction</code> test.</p>
    </video>
</a>

## Call to Action

### CI/Build Pipelines

What good is a testing framework if it isn't used? Get in touch if you want to
integrate WTF into your wallet's testing pipeline. We'll even build the
automation ourselves!

### Testing the Tests

We want to expand our tests for WTF, to catch issues with the framework itself.
To that end, if you work on a wallet that works offline (aside from the RPC
provider) and want to try out WTF, get in touch with us!

## Code Changes

 * [Upgraded to ganache 7.9][proof]!

## New Tests

 * [`eth_accounts` returns properly formatted hex strings][accounts].
 * [`eth_createAccessList` passes through value from ganache][accounts] ([skipped][access].)
 * [`eth_getProof` works for EOAs and contract storage][proof].
 * [`eth_call` can invoke a function and return the result][call].
 * [`eth_getLogs` respects block number and source address when returning blocks][call].
 * [`eth_maxPriorityFeePerGas` passes through value from ganache][call].
 * [`eth_sendRawTransaction` publishes transactions on-chain][call].
 * [`eth_gasPrice` passes through value from ganache][gas].
 * [`eth_estimateGas` passes through value from ganache][fee].
 * [`eth_feeHistory` passes through value from ganache][fee].
 * [`eth_sendTransaction` encodes call data to contracts][send].

[send]: https://github.com/wallet-test-framework/framework/commit/8e857f37c93ab57cbc5cf8120c0fc2571f106631
[fee]: https://github.com/wallet-test-framework/framework/commit/cf49df91a13b0da16419f128b519132c881304e8
[gas]: https://github.com/wallet-test-framework/framework/commit/d02c343295d93e4f7ef15b496688efbd689093dc
[call]: https://github.com/wallet-test-framework/framework/commit/7129096fb628bcd4aa41e0011436f1da1b9c7e7e
[proof]: https://github.com/wallet-test-framework/framework/commit/0439b7f42f7b2a13c5fef2c35a44a3cfcf20f0df
[accounts]: https://github.com/wallet-test-framework/framework/commit/307188aeb6ac0254fa2e0c808a2d6ed9158d1e16
[access]: https://github.com/trufflesuite/ganache/issues/1056
