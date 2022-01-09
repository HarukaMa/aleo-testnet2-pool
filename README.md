# Haruka's Aleo testnet2 mining pool

## Basic Info

This pool is for [Aleo Incentivized Testnet](https://www.aleo.org/post/incentivized-testnet-announcement) (testnet2).

The pool address is `aleo1harukzrnc7jfplxtn6005rs4xeglkrvvv0uwy56yzm0kkx062s9q3tdk8q`.

Information site will be [here](https://ap.mrx.im). New announcements will be posted on that site so make sure to check it often.

(The site is still WIP)

## Requirements

According to the Aleo team, **All pool participants will be required to complete KYC** after the testnet ends. It's currently not decided how it will work, but if you can't pass KYC procedure, your shares will be redistributed.

## Risk and Reward

All unofficial pools will compete for the top 100 rewards (which most likely will be 31250 Credits). There is also quadratic block rewards, but it will be considerably less than the rank reward. If the pool is unable to rank in the top 100, the payout will be very limited.

Every miner address needs to pass KYC in order to receive payment. If the pool itself somehow fails to pass KYC there will be no rewards to pay out(unlikely but possible).

The official pool might be more profitable considering you could individually get quadratic block rewards.

## Payout Structure

As there is no per-block rewards, the current plan is to distribute 99% of the block and rank rewards by pool shares. Please let me know if you have better ideas.

The pool records all valid shares even if the pool didn't win the block. (Current upstream code only counts the shares of won blocks.)

## How To Join

### Short version

Use the codebase at https://github.com/HarukaMa/snarkOS and join the pool at `69.10.36.174:4132`.

### Long version

The below instructions are mostly copied from [the official guide](https://github.com/AleoHQ/snarkOS) with modifications for this pool. 

### 1. Installation

Before beginning, please ensure your machine has `Rust v1.56+` installed. Instructions to [install Rust can be found here.](https://www.rust-lang.org/tools/install)

Start by cloning the snarkOS Github repository:
```
git clone https://github.com/HarukaMa/snarkOS
```

Next, move into the snarkOS directory:
```
cd snarkOS
```

**[For Ubuntu users]** A helper script to install dependencies is available. From the snarkOS directory, run:
```
./testnet2_ubuntu.sh
```

**[For other users]** Install the following packages:
```
clang
libssl-dev
pkg-config
```
The package names might be different on other distributions.

## 2. Run an Aleo Mining Node

Next, to generate an Aleo miner address, run:
```
cargo run --release -- experimental new_account
```
This will output a new Aleo account in the terminal.

**Please remember to save the account private key and view key.** The following is an example output:
```
 Attention - Remember to store this account private key and view key.

  Private Key  APrivateKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me
     View Key  AViewKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me
      Address  aleo1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Use Me For The Next Step
```

Next, to start a mining node, from the snarkOS directory, run:
```
./run-prover.sh
```
When prompted, enter your Aleo miner address:
```
Enter your Aleo miner address:
aleo1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

There will be no mining reports but you can track the state of the miner by reading the logs or checking for the shares on the pool info site.

## Contact

Discord: はるか#8264 or ping me in the Aleo server

Telegram: @harukaff_bot
