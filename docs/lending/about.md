<h1>About Lending</h1>



## Borrow - small draft

Experience the difference of Curve Lending. Enjoy the flexibility of DeFi borrowing with the added security of a system designed to protect you using [LLAMMA :llama:](./understanding-lending.md#llamma-and-liquidations).

Deposit collateral and borrow your desired asset.  You pay the **Borrow APY** based on the amount you borrow.

## Supply - small draft

Supply your assets to be lent out (borrowed by others) and enjoy receive the **Lend APY** plus **Rewards APR**.  Withdraw any un-lent assets at any time.

## How Curve Lending Works

Curve lending offers overcollateralized lending and borrowing of assets paired with crvUSD.  **crvUSD is not minted in Curve Lending**, all crvUSD is supplied by users.  All markets are **isolated**, ie. Supplied crvUSD collateral to the WETH market cannot be used to borrow CRV.  All markets are also **one-way**, ie. Supplied collateral cannot be lent out to another user.

Borrowing and Supplying Interest Rates are based solely on the Utilization (amount borrowed vs. amount supplied) of each lend pair.  Higher utilization means higher borrow and lend APYs.  At 0% Utilization borrowing rate is 0.1% while at 100% it is 1000%.

### Borrowing

When borrowing on Curve Lending, you are taking an overcollateralized loan against deposited assets (eg. borrowing crvUSD with CRV collateral).  You are charged the Borrow APY on the borrowed assets (eg. Borrowing APY increases crvUSD debt).  If your collateral drops in value and falls into your liquidation range, the platform will automatically begin trading your collateral for the borrowed asset as the price declines (eg. CRV swapped for crvUSD as CRV price declines).  The value of the converted collateral will remain yours minus trading fees (total collateral = CRV left + new crvUSD).

As long as the health factor is positive the position remains open.  It's valid to have all collateral converted to the borrowed asset with positive health ratio while the price is less than the liquidation range.  If this happens further price declines do not affect the position (eg. all CRV traded for crvUSD, and crvUSD collateral covers debt).  As prices increase through the Liquidition range any swapped collateral will be traded back for the deposited collateral through the liquidation range (eg. crvUSD collateral swapped back for CRV). You will only be hard liquidated if your health ratio reduces to 0.

In contrast, most other lending platforms will hard liquidate your collateral and terminate your loan if your loan falls below the minimum collateral ratio, even if only by a small amount for a brief time. This can be highly stressful for borrowers and lead to significant losses.

With Curve Lending's crvUSD soft liquidation, borrowers can rest easier knowing the platform is working to keep their loan safely collateralized while minimizing liquidation risk. Borrowing on Curve means less stress and a smoother experience.

### Supplying

By depositing and supplying assets on Curve Lending, you earn the **Lend APY** plus any **Rewards APR**.  You are able to withdraw a supplied asset provided there are enough available (unloaned) assets in the market.  However, if there are not enough available for withdrawal you can withdraw the maximum available amount and let the maximum Utilization rate incentivize others to repay, allowing a full withdrawal over time.

### More Information

For more information on basic concepts and borrowing and supplying please see [Curve Lending section within the Curve Resources](./understanding-lending.md).

For more technical information especially relating to the underlying smart contracts please see the [Lending section within the Curve Docs](https://docs.curve.fi/lending/overview)