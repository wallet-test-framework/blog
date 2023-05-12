+++
title="WTF News (Week 5)"
description="Fixed a lot of bugs and improved the UI."
date=2023-05-12

[taxonomies]
tags = ["Q1", "May"]
categories = ["status update"]
+++

Hello and welcome to issue number three of WTF News, our biweekly status update.

Since the last update, we've mostly been working on bug fixes, stability, and UI updates.

## Code Changes

 * [Add two new glue events/actions: `addEthereumChain` and `switchEthereumChain`][glue].
 * [Split page into three columns on wide screens][columns].
 * [Stricter lint rules][lints].
 * [Auto-scroll test resuts][scroll].
 * Added a utility for retrying assertions for a number of seconds.

## Bug Fixes

 * [Fixed "Order of mined blocks seems inconsistent"][ethers]. Likely related to how ethers.js fetches the block number. Fixed by calling `eth_blockNumber` directly.
 * [Fixed some][bug1] [JSON-RPC related][bug2] [bugs][bug3] (thanks to [Adam Hodges] of [coinbase] for reporting.)

## New Tests

None this update.

[glue]: https://github.com/wallet-test-framework/framework/commit/332c341cdbdde2218a52ebbaf2331d2d00b4ade5
[columns]: https://github.com/wallet-test-framework/framework/commit/0f7e863654ed6d18c987d0538b419e09f9ee5455
[lints]: https://github.com/wallet-test-framework/framework/commit/884a318f5cdd1b90c606f775dccaf4bdcb4c195a
[scroll]: https://github.com/wallet-test-framework/framework/commit/9f8d6b7dd16e392d34539e1378b77638da7e9aad
[ethers]: https://github.com/wallet-test-framework/framework/commit/e665ff070afd802eb0c73c8216d60b10ca7f8673
[coinbase]: https://www.coinbase.com/
[Adam Hodges]: https://twitter.com/asdag8
[bug1]: https://github.com/wallet-test-framework/framework/commit/9e00aab73c7c0c11fc981815b7e1ebb12c8c5139
[bug2]: https://github.com/wallet-test-framework/framework/commit/e420e22cbb2d6bd66c5bfa98eb09288ec306697d
[bug3]: https://github.com/wallet-test-framework/framework/commit/846047931c0116ed797d45e44e8857f9666f1efd
