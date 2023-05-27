+++
title="WTF News (Week 7)"
description="New tests; trying different libraries."
date=2023-05-26

[taxonomies]
tags = ["Q1", "May"]
categories = ["status update"]
+++

Hello and welcome to issue number four of WTF News, our biweekly status update.

This time around we've mostly focused on trying out alternatives to [ethers].
After wrestling with `eth_blockNumber` not returning the latest block number,
and other similar caching issues, we decided it would be best to try out a few
other frameworks to see what they offer. [@jakemoxey] suggested we try out
[viem], and it's been promising so far!

## Bug Fixes

 * [Don't kill web worker on error][error]. Ganache throws exceptions in some
   cases instead of returning an error code ([#34].)

## New Tests

 * [`eth_newFilter` doesn't return events from non-matching contracts][filter].
 * [`eth_newFilter` doesn't return events from non-matching topics][topic].
 * [Getting balance of contract accounts][contract].
 * [Getting nonce of externally owned accounts][eoa].

[ethers]: https://docs.ethers.org/v6/
[@jakemoxey]: https://twitter.com/jakemoxey
[viem]: https://viem.sh/
[error]: https://github.com/wallet-test-framework/framework/commit/76570875502ed3abc1ae6b7053184ad6b5ee4ebd
[#34]: https://github.com/wallet-test-framework/framework/issues/34
[filter]: https://github.com/wallet-test-framework/framework/commit/fe156324643f230b4862b1a8b6b2267708018e73
[topic]: https://github.com/wallet-test-framework/framework/commit/1e2dbd59ed8677820f3352d9eda7b6e92ac063d8
[contract]: https://github.com/wallet-test-framework/framework/commit/e20f9a7faf15b53fd6ce91e0c9e794ff98abdc03
[eoa]: https://github.com/wallet-test-framework/framework/commit/4704bf2183a6b34f3d0507b32fc9ee50865e74b4
