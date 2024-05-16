The following must be done on iOS and Android:

Peg In
- Amount lower than available
- Amount lower than the lower limit for peg in
- Swap all
- Some amount lower than swap all
- Verify peg-out amount in second field is rougly: (peg-in amount - btc fast fees - sideswap fee)
- Edge case: Minimal amount with fees higher than amount (if high fees exist at the time). Should throw error - otherwise would have negative peg-out amount.

Peg Out
- Amount lower than available
- Amount lower than the lower limit for peg in
- Swap all
- Some amount lower than swap all
- Verify peg-in amount in second field is rougly: (peg-out amount - liquid fee - sideswap fee) 
  (difference should be much lower than peg-out due to liquid fee being much lower)

LBTC to USDT
- Amount lower than available
- Amount lower than the lower limit for peg in
- Swap all
- Some amount lower than swap all

USDT to LBTC
- Amount lower than available
- Amount lower than the lower limit for peg in
- Swap all
- Some amount lower than swap all

OTHER
- [ ] Remove USDT from the asset list and confirm that it does not show in the swap list

- [ ] Confirm that swap combinations that are now allowed gives error (BTC<>USDT)

EDGE CASES

- Non-Confidential Tx Input: There is an edge case that popped up where a user had received a lbtc uxto that was not confidential. Because Sideswap only works with confidential inputs, there was an error thrown. The solution was for the user to send those funds to themselves using Aqua to create a confidential utxo that would then be used for the sideswap swap.
