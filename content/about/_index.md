+++
title = "About"
path = "about"

[extra]
date = 2023-03-24
+++

# Introduction

Wallets are the most important point of interaction for users on-boarding to the
Ethereum ecosystem, and there are a lot of different wallets. While wallets are
free to offer whatever advanced features they'd like, every wallet must support
the same basic operations like transfers, displaying balances, and so on. This
set of common features is the perfect place for automated testing.

Wallet Test Framework is that automated testing.

We'd like to see the UX quality among wallets improve, without a ton of
duplicated effort. That's why we are building Wallet Test Framework: an
automated testing framework that covers the basics, so wallet teams can build
value-add features without sacrificing their foundation.

# Learn More

If you'd like to learn more about our project structure or architecture,
our [Kick Off](/kick-off/) post has those details.

# In Action

This is what WTF looks like when running an `eth_sendTransaction` test with
<a href="https://frame.sh/" rel="nofollow">Frame</a> wallet and the manual glue.
The manual glue works with any[^1] wallet, as long as you can follow some
on-screen instructions.

<a href="/week-17/wtf-short.mp4">
    <video muted autoplay loop src="/week-17/wtf-short.mp4" style="max-width: 100%">
    <p>Demo video of an <code>eth_sendTransaction</code> test.</p>
    </video>
</a>

[^1]: Any wallet that supports custom RPC endpoints and injects
      `window.ethereum`. Surprisingly, some don't!
