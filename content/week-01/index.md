+++
title="WTF News (Week 1)"
description="Rewriting in not-Rust while playing with threads"
date=2023-04-14

[taxonomies]
tags = ["Q1", "April"]
categories = ["status update"]
+++

Hello and welcome to the first of hopefully many biweekly status updates! We're
going to try and write up a summary of the goings on in the Wallet Test
Framework, any features/tests that land, and any issues we discover.

## Code Changes

 * Rewrote the backend in TypeScript (instead of Rust.)
 * Updated [ethers.js] and [Ganache] to versions 6.3 and 7.7 respectively.
 * Switched from the [zora] testing library to the more well-known [Mocha] and
   [assert] libraries.
 * Use [esbuild] instead of [webpack].
 * [Move Ganache into its own WebWorker][worker].

## Bug Fixes

 * [Handle wallets that return immediately from `wallet_addEthereumChain`][add].

## New Tests

 * [`eth_blockNumber` and `eth_chainId`][6d2b11]
 * [`eth_getTransactionByHash` and `eth_getBlockByHash`][e1dacc]
 * [`eth_getBlockByNumber` and `eth_getBlockTransactionCountByHash`][2fc087]


[Ganache]: https://trufflesuite.com/ganache/
[ethers.js]: https://github.com/ethers-io/ethers.js/
[zora]: https://github.com/lorenzofox3/zora
[mocha]: https://mochajs.org/
[assert]: https://github.com/browserify/commonjs-assert
[esbuild]: https://esbuild.github.io/
[webpack]: https://webpack.js.org/
[add]: https://github.com/wallet-test-framework/framework/commit/3ca993d3e175e8ddcdd3b8e7234d3d267ce38483
[worker]: https://github.com/wallet-test-framework/framework/commit/ee64f255516f3cae66dd94606f0cb6ad078bf463
[6d2b11]: https://github.com/wallet-test-framework/framework/commit/6d2b11fb29dd9f6d345d5297dc3c331392595b2a
[e1dacc]: https://github.com/wallet-test-framework/framework/commit/e1daccd4adc0817530cdabff848a51b27f564d5b
[2fc087]: https://github.com/wallet-test-framework/framework/commit/2fc08714d46b32e0232e47333a4ca14699043833
