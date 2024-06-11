# SMOKE TEST
The purpose of a smoke test to test critical and major functionalities,
to quickly identify any major issues or showstoppers early in the testing process.

## AUTH
- [ ] Test Biometric On/Off

## WALLET
- [ ] Create new wallet
- [ ] Receive Tx
- [ ] Delete wallet
- [ ] Restore existing wallet with balances
    - [ ] Verify Balances
    - [ ] Verify Tx Details

## SEND
### QRSCANNER
- [ ] Test all assets
- [ ] Test bad addresses
- [ ] Bip21
    - [ ] Liquid non-LBTC with assetId goes to proper asset
    - [ ] BTC with Lightning fallback goes to Lightning Send
    - [ ] correctly parses amount (BTC, LBTC, Lightning, USDT...)
- [ ] Lightning Address
- [ ] LNURL-Pay

### BITCOIN
- [ ] Regular Send
- [ ] Verify fee rates show and change when tapped
- [ ] Send with custom fee
- [ ] Send All
- [ ] Fiat-denominated
- [ ] Verify tx shows up in tx history

### LBTC
- [ ] Regular Send
- [ ] Send All
- [ ] Fiat-denominated
- [ ] Verify tx shows up in tx history

### LIGHTNING
- [ ] Send various wallets
- [ ] Send Lightning Address
- [ ] Send LNURLp
- [ ] Send Aqua-to-Aqua (converts to LBTC send)
- [ ] Verify shows up in Tx Detail
- [ ] TEST REFUNDS: In "Experimental Features" you can force a send to fail and enter a refund state.
  - [ ] For v0.1.x, you will have to wait ~24 hours for the refund timelock to expire before testing if it broadcasts successfully
  - [ ] For v0.2.x, the refund should be near instant due to taproot cooperative keypath spend

### USDT
- [ ] Regular Send
    - [ ] NOTE: Redeposits don’t show up in tx history due to gdk
- [ ] Sideshift
    - [ ] Verify Sideshift order shows up in order history (currently in history button on USDT tx history screen), even if pending
    - [ ] Verify Send (no testnet unfortunately)

### OTHER
- [ ] Regular Send on any other asset
- [ ] Send All
- [ ] Fiat-denominated


## RECEIVE
### BITCOIN
- [ ] Address generation
- [ ] While setting amount, check fiat -> sats conversion is correct
- [ ] If amount is set, check it's encoded correctly in QR

### LBTC
- [ ] While setting amount, check fiat -> sats conversion is correct
- [ ] If amount is entered, the text displayed and copy button don’t include the BIP21, but Share and QR include the full bip21 with AMOUNT and ASSETID
    - [ ] Also test fiat-demoninated is converted to lbtc in bip21
- [ ] Switch between LBTC/Lightning is smooth and resets state

### LIGHTNING (Boltz)
- [ ] Invoice generated
- [ ] While setting amount, check fiat -> sats conversion is correct
- [ ] Check amount is corretly encoded in BIP21
- [ ] Generated Invoice has routingHints from Boltz (for aqua-to-aqua send)
- [ ] Success screen shows upon invoice payment
- [ ] NEED TO test claims with a variety of delays to mimic real world usage
  - [ ] Create invoice, background app for > 15min, pay invoice from another app, foreground app and verify that claim function runs and receive is completed.
  - [ ] Create invoice, close app. Pay invoice from another app. Open Aqua and verify that claim function runs and receive is completed.

### USDT
- [ ] Switch between networks is smooth and resets state
- [ ] If amount is set, check it's correctly encoded in BIP21
- [ ] Regular Receive
- [ ] Sideshift
    - [ ] Verify handles region not allowed error gracefully (switch vpn to US for this)
    - [ ] Verify order details display after fetch
    - [ ] Verify Eth vs Tron receive addresses are valid
    - [ ] Verify Sideshift order shows up in order history (currently in history button on USDT tx history screen), even if pending
    - [ ] Verify receive (no testnet unfortunately)

### OTHER
- [ ] Regular Receive for any other asset


## SWAPS
- [ ] Test Swap LBTC <> USDT
- [ ] Test Peg in
    - [ ] Verify peg-out amount in second field is rougly: (peg-in amount - btc fast fees - sideswap fee)
- [ ] Test Peg out
  - [ ] Verify peg-in amount in second field is rougly: (peg-out amount - liquid fee - sideswap fee) 
       -- difference should be much lower than peg-out due to liquid fee being much lower


## TX HISTORY/DETAIL SCREENS



## SETTINGS
- [ ] Invite others to AQUA
- [ ] Get Help
- [ ] Language
- [ ] Region (does nothing right now)
- [ ] Reference Rate
- [ ] Biometric Auth
- [ ] Dark/Light/Botev Mode
- [ ] Default Explorer
- [ ] Manage Assets - Add and verify they show with balances
- [ ] View Seed Phrase
- [ ] Bitcoin Chip - ?
- [ ] TOS/Privacy/Social Links



##  MARKETPLACE
- [ ] Test Meld flow


## UPDATING VERSIONS
- [ ] Test any issues that might come with updating versions. Looks for pending states carried over from previous version, such as pending swaps. Changes between versions in how we handle these states might affect outcomes.


## VPN + BAD/NO NETWORK CONDITIONS
- [ ] Test with a VPN on - some external endpoints have had issues with endpoints. 
    - Sideshift (USDt-Tether and Eth swaps) block US endpoints
- [ ] Test with bad network and no network
