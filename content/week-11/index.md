+++
title="WTF News (Week 11)"
description="Baby steps toward automation."
date=2023-06-26

[taxonomies]
tags = ["Q1", "June"]
categories = ["status update"]
+++

Hello and welcome to issue number six of WTF News, our biweekly status update.

Over the last two weeks, we've begun to focus on tests involving UI interaction,
like `eth_sendTransaction` and on the initial steps toward automating wallets.

## Code Changes

 * [Implement connecting to glue over WebSockets][glue-ws]. If you navigate to
   URLs of the form `https://127.0.0.1:3000/#glue=ws://127.0.0.1:3001/`, the
   tests will attempt to open a WebSocket connection to `127.0.0.1:3001` and
   issue commands to a glue instance there. The code is of prototype quality,
   and there is no documentation yet. For the adventurous, see the tests in
   [wallet-test-framework/glue-ws] for the gory details.

## Bug Fixes

 * During the transition to viem, we broke establishing the initial
   connection, so we [fixed it][first].
 * [`@wallet-test-framework/glue` didn't have any exports for Node][node].

## Upstream Issues

 * Incorrect type bounds for `register` ([elpheria/rpc-websockets#139].)

[first]: https://github.com/wallet-test-framework/framework/commit/591cc30cce10163c93ca2b9bbcbc3fdf5f8acf88
[node]: https://github.com/wallet-test-framework/glue/commit/27b406ee7880eae4227613bc8bc97be612345d4f
[elpheria/rpc-websockets#139]: https://github.com/elpheria/rpc-websockets/issues/139
[glue-ws]: https://github.com/wallet-test-framework/framework/commit/f126a4f0e72b08f402014fbc273b7e624632aee8
[wallet-test-framework/glue-ws]: https://github.com/wallet-test-framework/glue-ws
