+++
title="WTF News (Week 3)"
description="Broke some stuff, and added some glue."
date=2023-04-28

[taxonomies]
tags = ["Q1", "April"]
categories = ["status update"]
+++

Hello and welcome to issue number two of WTF News, our biweekly status update.
We've written more tests, new features, and broken more things than ever before!

## Known Issues

 * Order of mined blocks seems inconsistent. This affects tests for:
   `eth_getBlockByNumber`, `eth_getBlockByHash`,
   `eth_getBlockTransactionCountByHash`, `eth_getBlockTransactionCountByNumber`,
   and `eth_blockNumber`.

## Code Changes

 * [Added an introduction][welcome].
 * [Separate mocha output from introduction][intro].
 * [Dropped support for queueing RPC requests before the WebSocket is established][queue].
 * [Deployed a demo to Heroku][heroku].
 * Create the [`@wallet-test-framework/glue`][glue] package, and use it to
   [display instructions to the user][instruct].
 * [Automate compiling Solidity as part of the build][solc].

## Bug Fixes

None. We only added bugs this update.

## New Tests

 * [`eth_getBlockTransactionCountByHash`]
 * [`eth_getBlockTransactionCountByNumber`]
 * [`eth_newFilter`]

[solc]: https://github.com/wallet-test-framework/framework/commit/89892a7455723edcf4e6474de3c6b4009ab3c08e
[glue]: https://www.npmjs.com/package/@wallet-test-framework/glue
[instruct]: https://github.com/wallet-test-framework/framework/commit/f86bbe3b50bacd5228c0600598fb2e5f1a2c89aa
[heroku]: https://wallet-test-framework.herokuapp.com/
[queue]: https://github.com/wallet-test-framework/framework/commit/94c312bbcb483576adafded7251e92f88e35b31e
[intro]: https://github.com/wallet-test-framework/framework/commit/b1c6696ac3de5b6ce02d366959cf0f1a6a60d193
[welcome]: https://github.com/wallet-test-framework/framework/commit/6d3054e3e4eca4388791d032d4974ccf44704731
[`eth_getBlockTransactionCountByHash`]: https://github.com/wallet-test-framework/framework/commit/a6e2753fee9584a8f53ca999c704a65de7160da2
[`eth_getBlockTransactionCountByNumber`]: https://github.com/wallet-test-framework/framework/commit/009ae15b66e633f01aa7ae4cbad404604fd2dd0c
[`eth_newFilter`]: https://github.com/wallet-test-framework/framework/commit/16704f5cdaa1af2f8551756ed5cc8677d49c7151
