# Staking

Staking allows users to lock up their BLU tokens, in exchange for the staked BLU (sBLU), to earn rewards. The rewards come from proceeds of bond sales and liquidity provider fees.

### Staking Rewards

The staking reward is accrued and compounded every second to encourage and reward long-term stakers.

The continuous accrual mechanism means that:

* stakers do not have to waste gas claiming rewards, or
* be vulnerable to reward churning when malicious actors stakes during the ending period of an epoch to claim the reward, or
* miss out on an entire epoch of rewards when the protocol implements measures against the churning

In addition, the compounding mechanism encourages stakers to remain staked for the long term as short-term rewards are significantly lower.

![5000% APY Illustrated](<../.gitbook/assets/image (2).png>)

To illustrate the compounding effects using an APY of 5000%, if a staker started with 1000 BLU on day 1, he will only have 1379 BLU after the first month, but that would have compounded to 50,000 BLU over the course of the next 11 months!

### Passive Strategy

Once the BLU tokens are staked, the protocol will swap them for the staked BLU, sBLU, token. The sBLU token has a one-to-one exchange to the BLU token which increases in value each second.

When the tokens are staked, the staker does not need to do anything except to watch his balance grow and compound.

When you unstake, the sBLU token is swapped for an equal amount of BLU. That also means that these BLU are not accruing any rewards.

### Reward Rate

The reward rate for BLU is determined by the monetary policy set by the DAO. The level is dependent on the proceed from the bond sale, fees collected from the liquidity pool on the various stablecoins as well as the projected runway for sustaining the reward rate.
