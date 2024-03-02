+++
title="Test Report #2"
description="More wallets and more robots"
date=2024-03-01

[taxonomies]
tags = ["Q4", "March"]
categories = ["status update", "test report"]
+++

## Test Report

### Summary

<div class="report-holder">
<table class="report">
    <caption>
        <p>
            Wallet Test Framework –
            <a href="https://github.com/wallet-test-framework/framework/commit/94f9943cea81ccb8a3456ec031ad1bd00ee9a1f6">
                <code>94f9943cea81ccb8a3456ec031ad1bd00ee9a1f6</code>
            </a>
            <br>
            <a href="https://github.com/wallet-test-framework/framework">
                https://github.com/wallet-test-framework/framework
            </a>
        </p>
        <p>
            <em>Not a statement of a wallet's quality or correctness.</em>
        </p>
    </caption>
    <thead>
        <tr>
            <th>Wallet</th>
            <th>Automated</th>
            <th>Version</th>
            <th>Passing Tests</th>
            <th>Pass %</th>
            <th>Platform</th>
            <th>Notes</th>
        </tr>
    </thead>
    <tbody>
        <tr class="platinum">
            <th>Brave Wallet</th>
            <td>❌</td>
            <td></td>
            <td>61</td>
            <td>100%</td>
            <td>Brave v1.63.16</td>
            <td></td>
        </tr>
        <tr class="gold">
            <th>Frame</th>
            <td>❌</td>
            <td>0.6.8</td>
            <td>60</td>
            <td>98%</td>
            <td>Chromium 120.0.6099.129</td>
            <td>signTransaction unsupported</td>
        </tr>
        <tr class="gold">
            <th>Taho</th>
            <td>✔️</td>
            <td>0.57<a href="https://github.com/tahowallet/extension/pull/3737">+</a>
            </td>
            <td>60</td>
            <td>98%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>Changed definition of sign test to exclude hex</td>
        </tr>
        <tr class="gold">
            <th>Enkrypt</th>
            <td>❌</td>
            <td>1.33.0</td>
            <td>59</td>
            <td>97%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>signTransaction unsupported, doesn't show destination address</td>
        </tr>
        <tr class="gold">
            <th>Rainbow</th>
            <td>❌</td>
            <td>1.4.8</td>
            <td>56</td>
            <td>92%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>signTransaction opened, but was blank</td>
        </tr>
        <tr class="gold">
            <th>Backpack</th>
            <td>❌</td>
            <td>0.10.37</td>
            <td>56</td>
            <td>92%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>sendTransaction invalid length, sign just closed</td>
        </tr>
        <tr class="gold">
            <th>Opera Wallet</th>
            <td>❌</td>
            <td></td>
            <td>56</td>
            <td>92%</td>
            <td>Opera 107.0.5045.36</td>
            <td>Doesn't update balance before sending</td>
        </tr>
        <tr class="gold">
            <th>Coin98</th>
            <td>❌</td>
            <td>9.1.6</td>
            <td>55</td>
            <td>90%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>Doesn't display full addresses</td>
        </tr>
        <tr class="gold">
            <th>Aurox</th>
            <td>❌</td>
            <td>2.0.0</td>
            <td>53</td>
            <td>87%</td>
            <td>Chrome 122.0.6261.94</td>
            <td></td>
        </tr>
        <tr class="silver">
            <th>Metamask</th>
            <td>❌</td>
            <td>11.10.1</td>
            <td>48</td>
            <td>79%</td>
            <td>Chromium 120.0.6099.129</td>
            <td>signTransaction unsupported, logging/storage seems to lag behind chain</td>
        </tr>
        <tr class="silver">
            <th>Coinbase</th>
            <td>✔️</td>
            <td>3.57.0</td>
            <td>47</td>
            <td>77%</td>
            <td>Chromium 120.0.6099.129</td>
            <td>Doesn't show full addresses, can't differentiate sign/send transaction</td>
        </tr>
        <tr class="silver">
            <th>TokenPocket</th>
            <td>❌</td>
            <td>1.2.4</td>
            <td>46</td>
            <td>75%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>signTransaction unsupported</td>
        </tr>
        <tr class="silver">
            <th>xdefi</th>
            <td>❌</td>
            <td>&lt;28.3.6</td>
            <td>45</td>
            <td>74%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>Notably different signTransaction behaviour</td>
        </tr>
        <tr class="silver">
            <th>Trust</th>
            <td>❌</td>
            <td>2.7.2</td>
            <td>43</td>
            <td>70%</td>
            <td>Chrome 122.0.6261.94</td>
            <td>Doesn't support filters/subscriptions</td>
        </tr>
        <tr class="silver">
            <th>BlockWallet</th>
            <td>❌</td>
            <td>1.2.4</td>
            <td>40</td>
            <td>66%</td>
            <td>Chrome 122.0.6261.94</td>
            <td></td>
        </tr>
        <tr class="bronze">
            <th>OKX</th>
            <td>❌</td>
            <td>2.85.0</td>
            <td>22</td>
            <td>36%</td>
            <td>Chromium 120.0.6099.129</td>
            <td>As likely to be a bug in WTF as a wallet problem</td>
        </tr>
    </tbody>
</table>
</div>

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
wallets that don't support custom chains cannot be tested (omitted from this
table.)

For future reports, get in touch if you're interested in having your results
published (or if you'd prefer we didn't mention you.)

### Discussion

#### Automation

The most exciting part of this Test Report is the new "Automated" column.
Wallets with a "✔️ " (currently Taho and Coinbase) use the newest feature of WTF,
custom glue. Both of these wallets use [Selenium WebDriver]-based automation to
interact with their user interface to respond to prompts, like connecting or
signing transactions.

Automating wallets is the first step in our plan&mdash;removing humans from the
process means the tests can run unattended and regularly. Next, we plan to build
a reporting platform to track results over time and highlight regressions.

Here's what Taho looks like running the tests:

<a href="./taho.mp4">
    <video muted autoplay loop src="./taho.mp4" style="max-width: 100%">
    <p>Demo video of Taho with automation.</p>
    </video>
</a>

#### Common Issues

There are several issues that are hurting scores that we see across wallets:
incomplete information, unsupported features, minor deviations from the
JSON-RPC specification, and out-of-date information.

Far too many wallets (like Enkrypt, Coin98, etc.) do not display the source or
destination address when preparing a transaction. Commonly wallets will display
an abbreviated address (`0xabcd...1234`) and provide no way to view the full
value. This is a security issue, since it is relatively easy to mine addresses
that collide on only four bytes. Always provide a way to access the full value,
like in a tooltip or a "copy" button.

Perhaps following MetaMask's lead, many wallets do not support the
`eth_signTransaction` endpoint. Some other wallets do not support subscriptions.
While adding support for these features is nontrivial, it is important to
provide the same base level of functionality.

In other cases, wallets do provide a feature but do not follow the
specification. Coinbase, for example, omits the `0x` prefix on hexadecimal log
results and xdefi implements a very different `eth_signTransaction`. Having to
work around these differences increases the burden on dapp developers.

Finally, there is a whole class of bugs related to out-of-date information being
presented to the user. For example, Opera Wallet does not refresh balance
information while authorizing a transaction, preventing the user from completing
a transaction that would otherwise succeed.

### Conclusion

That's pretty much it for this Test Report. In the meantime,
[join us on Discord](https://allwallet.dev/)!

[find-wallet]: https://ethereum.org/en/wallets/find-wallet/
[architecture]: ../kick-off/
[Selenium]: https://www.selenium.dev/documentation/webdriver/
