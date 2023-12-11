+++
title="Year in Review (2023)"
description="What happened in 2023, and what we're planning for 2024"
date=2023-12-08

[taxonomies]
tags = ["December"]
categories = ["end of year"]
+++

Guess we failed pretty spectacularly in keeping up with the biweekly updates. Oh
well.

This post covers everything we've accomplished so far this year, and what we're
planning for next year.

## Year in Review

We began our year by rewriting our prototype for Wallet Test Framework in
TypeScript, to be more accessible to wallet developers. The original
implementation was half TypeScript and half Rust, and without a specific reason
to use Rust, we felt it more consistent to use TypeScript for everything. Around
this time, we also migrated to the Mocha testing framework.

Soon after, we set up our continuous integration pipeline to deploy the
framework to Heroku, making it easier to play with without having to build it.
We simplified the backend, and created scaffolding for glue implementations.

After some bug fixes and new tests, we migrated from ethers to viem, due to some
caching issues. We also introduced support for remote controlling wallets over
WebSockets.

After publishing our first [Test Report](@week-19), we moved full steam into
developing automation glue for Coinbase and Taho wallets. We've proven that our
tests are portable between wallets, and we've reported a handful of issues
upstream.

After a fairly successful first year, we're really looking forward to 2024!

## Roadmap for 2024

### Mobile Wallets

Our top priority for the upcoming year is to broaden our support for wallets,
especially mobile. Wallet Test Framework currently depends on `window.ethereum`,
pretty much limiting us to browser extension wallets. To better support the
Ethereum community, we need to integrate technologies like [WalletConnect],
[EIP-6963], and vendor-specific SDKs.

### Documentation & Collaboration

Wallet Test Framework is only useful if it is run, and can only find bugs for
areas it tests. Our second goal for 2024 is to write documentation for wallets,
EIP authors, and security experts so that they can all use and contribute easily
to the project.

We plan to write integration guides and documentation for wallets to make it as
easy as possible to run WTF as part of testing pipelines. This will cover topics
like writing the automated glue and adding vendor-specific tests.

Our biggest strength is that once a test is written, it's available to every
wallet using the framework. To take full advantage, we need to make it as easy
as possible for anyone—be it wallets themselves, EIP authors, or complete
outsiders—to write WTF tests. Documenting the test-writing process and having
clear guidelines for contributions are necessary to accomplish that goal.

### Transaction Decoding

This might be a bit of a stretch goal, but we'd like to start testing how
wallets decode the transactions of some popular applications. This is a wide
attack surface with plenty of room for quality assurance.

### [EIP-1193] Events

[EIP-1193] defines several events (like `connect` or `accountsChanged`) that
aren't covered by the current tests. Emitting these events is essential for
responsive application development, so we'd like to expand our coverage in this
area.

### Account Abstraction Wallets

The world of account abstraction wallets has exploded since the introduction
of [ERC-4337]. We'd like to explore expanding our tests to cover them.

### Statistics & Reporting

We'd like to develop a dashboard showing the scores of wallets over time, as
well as automation implementation status, and enabled test suites. These
statistics will allow us to gauge how much of an impact Wallet Test Framework
has on the ecosystem.

## Supporters

We want to give a huge thank you to the Ethereum Foundation's Ecosystem Support
Program and to the donors on Gitcoin for helping to fund our work so far. We'd
also like to thank Coinbase for being very supportive and responsive when
reporting issues.

[WalletConnect]: https://walletconnect.com/
[EIP-6963]: https://eips.ethereum.org/EIPS/eip-6963
[EIP-1193]: https://eips.ethereum.org/EIPS/eip-1193
[ERC-4337]: https://eips.ethereum.org/EIPS/eip-4337
