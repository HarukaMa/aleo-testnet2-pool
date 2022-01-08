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

This section is intentionally left blank as I'm still building the infrastructure needed to run the pool. Stay tuned.

## Contact

Discord: はるか#8264 or ping me in the Aleo server

Telegram: @harukaff_bot
