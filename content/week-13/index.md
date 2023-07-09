+++
title="WTF News (Week 12)"
description="What's up with sign transaction?"
date=2023-07-09

[taxonomies]
tags = ["Q2", "July"]
categories = ["status update"]
+++

Hello and welcome to issue number seven of WTF News, our biweekly status update.

This release introduces the first interactive tests, and our first major
inconsistencies between wallets: `eth_sign` and `eth_signTransaction`.

Some wallets have treated `eth_sign` as a "sign raw data" operation, while
others implement it as "sign prefixed text", while still others disable it
entirely. Similarly, `eth_signTransaction` is often not supported at all.

For these cases, we've chosen to test for the behaviour specified in the
[JSON-RPC] specification and treat anything different as a test failure.

## Call to Action

We want to expand our tests for WTF, to catch issues like last update's
connection issue. To that end, if you work on a wallet that works offline (aside
from the RPC provider) and want to try out WTF, get in touch with us!

## Code Changes

 * Support for [signing messages][msg] and [sending transactions][tx] in the
   glue.

## New Tests

 * [`eth_sign` creates a valid signature with prefix][sign].
 * [`eth_sendTransaction` creates and publishes a transaction][send].


[sign]: https://github.com/wallet-test-framework/framework/commit/16fd0b4be66e792879519a4c93928bfb424e7dcb
[send]: https://github.com/wallet-test-framework/framework/commit/1d43c057a9f86e0ee46e044b5d5d4ce82062b664
[msg]: https://github.com/wallet-test-framework/glue/commit/068fa890fed818d4248d1e01ac204df65f2c68ad
[tx]: https://github.com/wallet-test-framework/glue/commit/1f5d4dd51a67d9d3da3b0b796b7e483cfb69dace
[JSON-RPC]: https://ethereum.github.io/execution-apis/api-documentation/
