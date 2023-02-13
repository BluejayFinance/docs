# Bonding

Bonding is a process to allow Bluejay to acquire its own liquidity and reserve assets (ie DAI) and bring stablecoins to the peg by selling BLU at a discount. There are two main types of bonds on Bluejay, treasury bonds, and stabilizing bonds. For both types of bonds, the user gets discounted BLU after a fixed vesting period. The only difference is that treasury bonds raise assets for the treasury directly while stabilizing bonds help to peg issued stablecoins to their prices.

When bonders purchase a bond from the protocol, they will be quoted the term of the bond such as the discounted BLU price, the vesting period, and the amount of BLU claimable when the bond matures. The bond will vest linearly over the vesting period, allowing the bonder to claim any vested BLU as it matures, and the full amount when the entire period is up.

### Treasury Bonds

The objective of these bonds is to allow the protocol to acquire its own liquidity which in turn will be used productively for minting, backing and providing liquidity for stablecoins which in turn generates revenue through swap fees and arbitrage for the protocol.&#x20;

More information about the treasury bonds can be found in the core concept section:

{% content-ref url="../blustables-core-concepts/treasury-bonds.md" %}
[treasury-bonds.md](../blustables-core-concepts/treasury-bonds.md)
{% endcontent-ref %}

### Stabilizing Bonds

The objective of stabilizing bonds is to bring the various stablecoins' prices to their peg through automatic open market operations (by buying or selling bluStables from the market).

More information about the stabilizing bonds can be found in the core concept section:

{% content-ref url="../blustables-core-concepts/stabilizing-bond.md" %}
[stabilizing-bond.md](../blustables-core-concepts/stabilizing-bond.md)
{% endcontent-ref %}

### Choosing your bonds

The different bonds will be quoted on the protocol website along with the APY. As a protocol user, you will should pick the bond which presents the highest APY for you. Whether the bond is a treasury bond or a stabilizing bond does not affect the way you interact with it, you simply swap your reserve assets (or LP token) for discounted BLU.
