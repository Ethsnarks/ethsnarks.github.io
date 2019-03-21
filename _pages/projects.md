---
permalink: /
title: "Ethsnarks Projects"
excerpt: "ETHSNARKS Projects"
author_profile: false
redirect_from: 
  - /projects/
  - /projects.html
---

Ethsnarks is comprised of a main repository and several other repositories which use the main repository as a git submodule.

## [ethsnarks](https://github.com/HarryR/ethsnarks)

The core repository, includes implementations of all algorithms and common code, the build system and tests. It is implemented in C++ using CMake as a build system. It can be built on Linux, OSX and Windows - however, testing is limited to Linux and OSX so Windows support may be subtly broken.

## [ethsnarks-emscripten](https://github.com/Ethsnarks/ethsnarks-emscripten)

Builds libsnark and Ethsnarks for WebAssembly using Emscripten.

However, libgmp compiled to WebAssembly using Emscripten is very slow, around 40x slower than native. Given that around 60% of the proving time is GMP modulo multiplication operations this is a significant performance impact which limits the usefulness of the Emscripten port of Ethsnarks.

# Examples

## [ethsnarks-hashpreimage](https://github.com/Ethsnarks/ethsnarks-hashpreimage)

Ethereum compatible example project, demonstrates how to prove you know the secret pre-image for a SHA2-256 hash, integrates with an on-chain smart contract with Truffle, Javascript and Python support.

## [ethsnarks-snasma](https://github.com/Ethsnarks/ethsnarks-snasma)

Demonstrates the 'roll_up' transaction aggregator pattern for computational compression - using only three fields 'from index', 'to index' and 'amount' for each transaction the zkSNARK circuit ensures that a valid signature for the 'from' account in a merkle tree is used - it then updates the merkle tree and provides the new root.

## [ethsnarks-miximus](https://github.com/HarryR/ethsnarks-miximus)

Ethereum compattible example project, provides an anonymised fixed-denomination coin mixing service for Ethereum. Includes Truffle, Javascript, Solidity and Python support.

## [ethsnarks-pepper-extgadget](https://github.com/Ethsnarks/ethsnarks-pepper-extgadget)

Example of integrating Ethsnarks with the Pepper project to provide 'exogenous gadgets'.

# High-level languages

## [ethsnarks-il](https://github.com/Ethsnarks/ethsnarks-il)

This project aims to separate the 'intermediate language' part of the Ethsnarks repository (which started as part of the jsnark and pinocchio compatibility efforts) into its own repository.

## [ethsnarks-jsnark](https://github.com/Ethsnarks/ethsnarks-jsnark)

Initial attempt at integration between [jsnark](https://github.com/akosba/jsnark) and Ethsnarks, the circuits compiled using jsnark or [xjsnark](https://github.com/akosba/xjsnark) can be compiled, proved and run using Ethsnarks - which in turn is compatible with Ethereum.

## [ethsnarks-sfdl](https://github.com/Ethsnarks/ethsnarks-sfdl)

Initial attempt at porting the FairPlay MPC language called 'Secure Function Definition Language' to be compatible with Ethsnarks and Ethereum.

## [ethsnarks-pinocchio](https://github.com/Ethsnarks/ethsnarks-pinocchio)

Initial attempt to add support for the Pinocchio C to QAP compiler and intermediate language to Ethsnarks.
