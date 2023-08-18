+++
title="WTF News (Week 19)"
description="Are you ready to rumble?"
date=2023-08-18

[taxonomies]
tags = ["Q2", "August"]
categories = ["status update", "test report"]
+++

Hello and welcome to issue number nine of WTF News, our biweekly status update.

Over the last two weeks, we ran a handful of wallets through their paces, and
today we can reveal the results! Spoiler alert, but there were more issues in
our tests than in the best scoring wallets.

First, the regular status update!

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

 * [Upgraded to viem 1.6][viem]!

## Bug Fixes

 * [Use smaller integers to make ganache happy][smallint].
 * [Send WebSocket pings to keep the connection alive][ping].
 * [Use `from` instead of `account` in `eth_signTransaction`][from].
 * [Use hex instead of decimal in `eth_signTransaction`][hex].
 * [Convert `BigInt` to hex in `eth_getProof`][proof].
 * [Actually put `jsonrpc` in responses to the wallet][jsonrpc].
 * [Handle race condition when falling back to adding a chain manually][chain].

## Upstream Issues

 * [`eth_call` unclear when `Block` parameter is omitted][block].

## Test Report

### Summary

<div class="report-holder">
<table class="report">
    <caption>
        <p>
            Wallet Test Framework –
            <a href="https://github.com/wallet-test-framework/framework/commit/f999503092a10f2b409b5cc733db065c124e56e5">
                <code>f999503092a10f2b409b5cc733db065c124e56e5</code>
            </a>
            <br>
            <a href="https://github.com/wallet-test-framework/framework">
                https://github.com/wallet-test-framework/framework
            </a>
        </p>
        <p>
            <em>Not a statement of a wallet’s quality or correctness.</em>
        </p>
    </caption>
    <thead>
        <tr>
            <th>Wallet</th>
            <th>Version</th>
            <th>Connection</th>
            <th>Passing Tests</th>
            <th>Pass %</th>
            <th>Platforms</th>
            <th>Browser</th>
            <th>Notes</th>
        </tr>
    </thead>
    <tbody>
        <tr class="platinum">
            <th>Brave Wallet</th>
            <td></td>
            <td>EIP-3085</td>
            <td>61</td>
            <td>100%</td>
            <td>Browser</td>
            <td>Brv 1.57.42</td>
            <td></td>
        </tr>
        <tr class="platinum">
            <th>Taho</th>
            <td>0.46.1</td>
            <td>EIP-3085</td>
            <td>61</td>
            <td>100%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>Had to impersonate chainlist.org</td>
        </tr>
        <tr class="gold">
            <th>Frame</th>
            <td>0.6.7</td>
            <td>EIP-3085</td>
            <td>60</td>
            <td>98%</td>
            <td>Desktop</td>
            <td>Ff 102.14.0esr (64-bit)</td>
            <td>Missing signTransaction</td>
        </tr>
        <tr class="gold">
            <th>Enkrypt</th>
            <td>1.24.0</td>
            <td>Manual</td>
            <td>59</td>
            <td>97%</td>
            <td>Extension</td>
            <td>Ff 102.14.0esr (64-bit)</td>
            <td>Attempted EIP-3085, but popup doesn’t show RPC url</td>
        </tr>
        <tr class="silver">
            <th>Coinbase</th>
            <td>3.30.2</td>
            <td>EIP-3085</td>
            <td>48</td>
            <td>79%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>Missing hex prefix in logs</td>
        </tr>
        <tr class="silver">
            <th>Metamask</th>
            <td>10.34.0</td>
            <td>EIP-3085</td>
            <td>48</td>
            <td>79%</td>
            <td>Extension</td>
            <td>Ff 102.14.0esr (64-bit)</td>
            <td></td>
        </tr>
        <tr class="bronze">
            <th>OKX</th>
            <td>2.58.1</td>
            <td>EIP-3085</td>
            <td>18</td>
            <td>30%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>Tests stopped running somewhere around getFilterChanges</td>
        </tr>
        <tr class="bronze">
            <th>TokenPocket</th>
            <td>1.1.19</td>
            <td>EIP-3085</td>
            <td>15</td>
            <td>25%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>Tests stopped running somewhere around getFilterChanges</td>
        </tr>
        <tr class="garbage">
            <th>Argent X</th>
            <td>5.7.2</td>
            <td>Can’t Connect</td>
            <td>0</td>
            <td>0%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>No window.ethereum</td>
        </tr>
        <tr class="garbage">
            <th>Bitkeep</th>
            <td>1.4.8</td>
            <td>Can’t Connect</td>
            <td>0</td>
            <td>0%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>Attempted EIP-3085, and Manual, but got system error</td>
        </tr>
        <tr class="garbage">
            <th>Sequence</th>
            <td>2.0.4</td>
            <td>Can’t Connect</td>
            <td>0</td>
            <td>0%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>Cannot add custom chains</td>
        </tr>
        <tr class="garbage">
            <th>Exodus</th>
            <td>23.8.14</td>
            <td>Can’t Connect</td>
            <td>0</td>
            <td>0%</td>
            <td>Extension</td>
            <td>Chr 115.0.5790.170</td>
            <td>Cannot add custom chains</td>
        </tr>
    </tbody>
</table>
</div>

The astute reader may notice that there are in fact 62 tests in the repository
at that commit. Our `eth_getProof` test is broken, and we are excluding it from
this report.

### Disclaimer

Our intent is not to claim that certain wallets are better than others, and a
low score here is as likely to indicate that our tests have problems as it
is to indicate bugs in a wallet. We're very interested in improving scores
across the board, so we're happy to accept contributions to fix tests and just
as happy to help debug.

### Wallet Selection

Very little of this report is scientific/rigorous, and the wallet selection
process was no exception. We chose a few wallets we're familiar with, and a
small sampling of random wallets from the [Find an Ethereum Wallet][find-wallet]
list.

Because Wallet Test Framework only supports `window.ethereum` so far, we're
limited to wallets that provide it; that pretty much excludes mobile wallets for
the time being. Our [architecture] requires connecting to a custom chain, so
wallets that don't support custom chains cannot be tested (labelled with `Can't
Connect` in the table.)

For future reports, get in touch if you're interested in having your results
published (or if you'd prefer we didn't mention you.)

### Discussion

Congratulations to [Brave] and [Taho] for getting perfect scores! Considering
this was our first time trying them out with the Framework (we've been using
[Frame] to develop), this was quite surprising.

#### `eth_signTransaction`

This is a contentious endpoint that we've [discussed previously](../week-13).
Very few wallets support `eth_signTransaction`, mostly by choice.

Interestingly, this was Frame's only failure: instead of signing in the wallet,
Frame passes these requests through to the RPC provider.

#### Caching

> There are only two hard things in Computer Science: cache invalidation and
> naming things. _Phil Karlton_

Caching is hard. [We've been bitten by it](../week-07/). In a space where you
have to pay for every API request, but your users expect a free wallet
experience, caching is a necessary evil.

We suspect, but haven't verified for all wallets, that many of the test failures
are caused by stale values cached by wallets.

In the case of `eth_call`, we have verified that MetaMask specifies an old block
number, causing a call into a freshly deployed contract to fail. This is
unlikely to cause major issues on a real network with many seconds between
blocks, but the tests mine blocks much more frequently, triggering the issue.
Regardless, we're following up with their team to see what we can do.

#### Post-merge Endpoints

Some of the newer endpoints like `eth_maxPriorityFeePerGas` aren't yet supported
in all wallets. Expect these tests to start passing as they are implemented.

### Future Plans

We'll continue adding tests, and we'll try to run through this report somewhat
regularly. That said, this is entirely a manual process. Once wallets start
running WTF as part of their continuous integration processes, we can make some
pretty graphs, include more wallets, and make reports more often.

In the meantime, [join us on Discord](https://allwallet.dev/)!

[viem]: https://github.com/wallet-test-framework/framework/commit/b55b9729be2b82bd113ab821697dc77fc1e876b1
[smallint]: https://github.com/wallet-test-framework/framework/commit/f999503092a10f2b409b5cc733db065c124e56e5
[ping]: https://github.com/wallet-test-framework/framework/commit/801d8f9ca0e081a130e04f1ba91121fc29de84c2
[from]: https://github.com/wallet-test-framework/framework/commit/a86d4284e9fbada0653105a08deab7b9f88569c1
[hex]: https://github.com/wallet-test-framework/framework/commit/759cbe74604ac56d1f75a367bf285423265625d6
[proof]: https://github.com/wallet-test-framework/framework/commit/52bb9661d135719e6c092a9e87dcd21e577e125c
[jsonrpc]: https://github.com/wallet-test-framework/framework/commit/aab09bd782a75f513d2e8ab6678a384ba32b15ce
[chain]: https://github.com/wallet-test-framework/framework/commit/22a116d8754f379c44745d7231e14a1442f9f1fd
[find-wallet]: https://ethereum.org/en/wallets/find-wallet/
[block]: https://github.com/ethereum/execution-apis/issues/461
[Brave]: https://brave.com/wallet/
[Taho]: https://taho.xyz/
[Frame]: https://frame.sh/
[architecture]: ../kick-off/
