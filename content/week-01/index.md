+++
title="WTF News (Week 1)"
description="Rewriting in not-Rust while playing with threads"
date=2023-04-13
draft=true

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


[Ganache]: https://trufflesuite.com/ganache/
[ethers.js]: https://github.com/ethers-io/ethers.js/
[zora]: https://github.com/lorenzofox3/zora
[mocha]: https://mochajs.org/
[assert]: https://github.com/browserify/commonjs-assert
[esbuild]: https://esbuild.github.io/
[webpack]: https://webpack.js.org/
[add]: https://github.com/wallet-test-framework/framework/commit/3ca993d3e175e8ddcdd3b8e7234d3d267ce38483
[worker]: https://github.com/wallet-test-framework/framework/commit/ee64f255516f3cae66dd94606f0cb6ad078bf463
