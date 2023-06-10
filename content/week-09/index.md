+++
title="WTF News (Week 9)"
description="Migrating to viem, exception handling, and of course tests!"
date=2023-06-09

[taxonomies]
tags = ["Q1", "June"]
categories = ["status update"]
+++

Hello and welcome to issue number five of WTF News, our biweekly status update.

Since our last post, we've settled on [viem] for the time being. It fixed our
caching issues, and has excellent TypeScript support!

## Code Changes

 * [Migrate from ethers to viem][migrate].
 * Pass errors from Ganache [over `postMessage`][postMessage] then
   [the WebSocket][WebSocket].
 * [Increase the slow test timeout][slow].
 * [Disable minify by default][tx-hash]. Now test source code is understandable
   in Mocha's HTML output!

## New Tests

 * [`eth_getTransactionCount` for contract accounts][count].
 * [`eth_getCode` returns the contract's bytecode][code].
 * [`eth_newBlockFilter` returns new blocks][slow].
 * [`eth_getStorageAt` can read contract storage][storage].
 * [`eth_getTransactionByBlockHashAndIndex`][tx-hash] and
   [`eth_getTransactionByBlockNumberAndIndex`][tx-num] get transactions.
 * [`eth_getTransactionReceipt`][tx-num] can get receipts.
 * A [whole] [lot] of [filter tests].

## Upstream Issues

 * Ganache returns `null` from several endpoints, and it's unclear if that's
   allowed in the specification ([ethereum/execution-apis#288].)
 * Getting transactions by index beyond the end of the block throws an
   exception ([trufflesuite/ganache#4435].)

[viem]: https://viem.sh/
[migrate]: https://github.com/wallet-test-framework/framework/commit/5413056077f7e7905bbb0fe238dfa3ebfcb85b2d
[postMessage]: https://github.com/wallet-test-framework/framework/commit/6c91a202d1bb8bb206f6fd0a9fbdbac07db42d80
[WebSocket]: https://github.com/wallet-test-framework/framework/commit/4669cc8e25ace968c2c9e125d42f3cdf8d6b6354
[count]: https://github.com/wallet-test-framework/framework/commit/0dd0c3c4078e5b8fca0ca9a353fb5da6878bf226
[code]: https://github.com/wallet-test-framework/framework/commit/562b2fe9a01ece1f8a37720ad2e1b36d747497e7
[slow]: https://github.com/wallet-test-framework/framework/commit/e1e48ee26ed7b79a9b02c5d2d72fcc44ef46251f
[storage]: https://github.com/wallet-test-framework/framework/commit/a727791f50613c91a90b9456b6af1b20d64ceab4
[tx-hash]: https://github.com/wallet-test-framework/framework/commit/e638787b7b5ab642b38a1060f73c798349aa00ad
[tx-num]: https://github.com/wallet-test-framework/framework/commit/bd2df0747e43f2a937939fb98b453ee405d65eba
[whole]: https://github.com/wallet-test-framework/framework/commit/f47c1aa3e950f6dad78c0ec7544f14e2b95834de
[lot]: https://github.com/wallet-test-framework/framework/commit/aecd12cff2fc2cbcfbc7ffcfac8a0f2ae4eea185
[filter tests]: https://github.com/wallet-test-framework/framework/commit/ab9b156a76199bd80be8dcf6244b4f99405afda6
[ethereum/execution-apis#288]: https://github.com/ethereum/execution-apis/issues/288
[trufflesuite/ganache#4435]: https://github.com/trufflesuite/ganache/issues/4435
