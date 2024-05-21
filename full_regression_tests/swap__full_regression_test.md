## The following must be done on iOS and Android:

Peg In
- [ ] Amount lower than available
- [ ] Amount lower than the lower limit for peg in
- [ ] Swap all
- [ ] Some amount lower than swap all
- [ ] Verify peg-out amount in second field is roughly: (peg-in amount - btc fast fees - sideswap fee)
- [ ] Verify that the estimated receive amount in this second field matches the amount displayed on the review screen
- [ ] High fees: Test this during high fee environments (issue to mock this: https://github.com/jan3dev/aqua-dev/issues/892)
- [ ] Edge case: Minimal amount with fees higher than amount (if high fees exist at the time). Should throw error - otherwise would have negative peg-out amount.

Peg Out
- [ ] Amount lower than available
- [ ] Amount lower than the lower limit for peg in
- [ ] Swap all
- [ ] Some amount lower than swap all
- [ ] Verify peg-in amount in second field is roughly: (peg-out amount - liquid fee - sideswap fee) 
  (difference should be much lower than peg-out due to liquid fee being much lower)
- [ ] Verify that the estimated receive amount in this second field matches the amount displayed on the review screen

LBTC to USDT
- [ ] Amount lower than available
- [ ] Amount lower than the lower limit for peg in
- [ ] Swap all
- [ ] Some amount lower than swap all

USDT to LBTC
- [ ] Amount lower than available
- [ ] Amount lower than the lower limit for peg in
- [ ] Swap all
- [ ] Some amount lower than swap all

OTHER
- [ ] Remove USDT from the asset list and confirm that it does not show in the swap list

- [ ] Confirm that swap combinations that are now allowed gives error (BTC<>USDT)

EDGE CASES

- [ ] Non-Confidential Tx Input: There is an edge case that popped up where a user had received a lbtc uxto that was not confidential. Because Sideswap only works with confidential inputs, there was an error thrown. The solution was for the user to send those funds to themselves using Aqua to create a confidential utxo that would then be used for the sideswap swap.

## Notes:
Swaps between BTC <> LBTC use peg-in and peg-out through Sideswap api. In the future this may change to Boltz atomic swaps.
LBTC <> USDt uses Sideswap as well but use a combined pset method.

For peg-in and peg-out, as of May 2024 the amount logic is as follows:
- User enters 10,000 sats to peg in or out, for example
- The amount calculated in the Receive field is an estimate for this 10,000 - onchain fee - sideswap fee (0.1%)
  eg 10,000 - 700 - 10 = 9,290
- However, the amount we send to sideswap will be 9,300, because they then take their fee out when on the second tx
- The user doesn't get 9,290 though, because there will also be a second tx on the receiving chain, and sideswap will take that fee out as well. We don't include this second fee in the Receive Amount prompt because for peg-out this second fee will be btc onchain and sideswap decides the fee rate

