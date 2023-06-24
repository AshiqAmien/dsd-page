---
layout: default
title: "instructions.txt"
tags: instructions
---

# Decently Safe DeFi ⚒️

Decently Safe DeFi is released with 4 challenges based on [Abracadabra.money's](https://abracadabra.money/) CauldronV4 and DegenBox contracts.

[![Twitter Follow](https://img.shields.io/twitter/follow/ngp2311?label=Follow%20me%20%40AshiqAmien&style=social)](https://twitter.com/AshiqAmien)

### Acknowledgement
*Big thanks to [Tincho](https://twitter.com/tinchoabbate) who created the [first version of this game](https://github.com/tinchoabbate/damn-vulnerable-defi/tree/v2.0.0) and to all the fellows behind the [Foundry Framework](https://github.com/gakonst/foundry/graphs/contributors). Further thanks to [Nicolás García](https://github.com/nicolasgarcia214), who ported Damn Vulnerable Defi to foundry.*

Decently Safe DeFi is an unofficial fork of [Damn Vulnerable DeFi](https://damnvulnerabledefi.xyz), a wargame to learn offensive security of DeFi smart contracts.

Decently Safe Defi is different from Damn Vulnerable Defi since its challenges are based on dead end bug leads of real protocols. The challenges are created by subtly removing the last line of defence, or reversing a minor misconfiguration of a protocol to produce a critical result.

## How To Play 🕹️

1.  **Install Foundry**

First run the command below to get foundryup, the Foundry toolchain installer:

``` bash
curl -L https://foundry.paradigm.xyz | bash
```

Then, in a new terminal session or after reloading your PATH, run it to get the latest forge and cast binaries:

``` console
foundryup
```

2. **Clone This Repo and install dependencies**
``` 
git clone https://github.com/nicolasgarcia214/damn-vulnerable-defi-foundry.git
cd damn-vulnerable-defi-foundry
forge install
```
3. **Code your solutions in the provided `[NAME_OF_THE_LEVEL].t.sol` files (inside each level's folder in the test folder)**
4. **Run your exploit for a challenge**
```
forge test --match-contract [ChallengeName] -vvvv
```
or
```
./run.sh [LEVEL_FOLDER_NAME]
./run.sh [CHALLENGE_NUMBER]
./run.sh [4_FIRST_LETTER_OF_NAME] 
```
If the challenge is executed successfully, you've passed!🙌🙌

### Tips and tricks ✨
- In all challenges you must use the account called attacker. In Forge, you can use the [cheat code](https://github.com/gakonst/foundry/tree/master/forge#cheat-codes) `prank` or `startPrank`.
- To code the solutions, you may need to refer to the [Foundry Book](https://book.getfoundry.sh/).
- In some cases, you may need to code and deploy custom smart contracts.

### Preinstalled dependencies

`ds-test` for testing, `forge-std` for better cheatcode UX, and `openzeppelin-contracts` for contract implementations.
