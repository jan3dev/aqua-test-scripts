The following must be done on iOS and Android:

Peg In
- amount lower than available
- amount lower than the lower limit for peg in
- swap all
- some amount lower than swap all†

Peg Out
- amount lower than available
- amount lower than the lower limit for peg in
- swap all
- some amount lower than swap all

LBTC to USDT
- amount lower than available
- amount lower than the lower limit for peg in
- swap all
- some amount lower than swap all

USDT to LBTC
- amount lower than available
- amount lower than the lower limit for peg in
- swap all
- some amount lower than swap all

- [ ]Remove USDT from the asset list and confirm that it does not show in the swap list

- [ ]Confirm that swap combinations that are now allowed gives error (BTC<>USDT)

EDGE CASES

- Non-Confidential Tx Input: There is an edge case that popped up where a user had received a lbtc uxto that was not confidential. Because Sideswap only works with confidential inputs, there was an error thrown. The solution was for the user to send those funds to themselves using Aqua to create a confidential utxo that would then be used for the sideswap swap.
