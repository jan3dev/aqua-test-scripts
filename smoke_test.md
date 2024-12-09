# SMOKE TEST
The purpose of a smoke test to test critical and major functionalities,
to quickly identify any major issues or showstoppers early in the testing process.

## FRESH INSTALL VS UPDATING VERSIONS
- [ ] Test fresh install vs updating versions
- [ ] Test any issues that might come with upgrading aqua versions. Looks for pending states carried over from previous version, such as pending swaps. Changes between versions in how we handle these states might affect outcomes.
- [ ] 🚨🚨 A big issue to look out for on upgrading aqua versions is that if the user is logged in on version A, when upgrading to version B they ARE NOT kicked out and have to enter their seed again. Some users won't have their seed backed up and if this happens they will lose their sats! 🚨🚨

## HOME SCREEN
### TOTAL BALANCE
- [ ] On first app open wallet header shows total balance if balance > 0
- [ ] In settings, change reference currency and total balance currency should update accordingly
- [ ] Tap on total balance amount and wallet header should switch to btc price
- [ ] Close and re-open the app, last choice should be remembered and btc price shown by default
      
## AUTH
- [ ] Test Biometric On/Off

## WALLET
- [ ] Create new wallet
- [ ] Receive Tx
- [ ] Close app and reopen. Verify that a backup seed reminder shows (only happens on new wallets after you receive your first sats)
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
- [ ] Send LNURL
- [ ] Send Aqua-to-Aqua (converts to LBTC send)
- [ ] Verify shows up in Tx Detail
- [ ] TEST REFUNDS: In "Experimental Features" you can force a send to fail and enter a refund state.
    - [ ] The refund should be near instant due to taproot cooperative keypath spend
- [ ] Send with Lightning and check that the blue success screen first displays 'You're sending...' and then updates to 'You've sent' when the transaction is complete.

### USDT
- [ ] Regular Send
   NOTE: Redeposits don’t show up in tx history due to gdk
- [ ] USDt Fee
    - [ ] Wallet with USDt but 0 LBTC, verify USDt sends work with USDt fees. LBTC fee selector should be disabled.
    - [ ] Wallet with LBTC but 0 USDt, verify that all liquid sends work, including USDt, allowing user to send with LBTC fees. USDt fee selector should be disabled.
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
  - [ ] From Send Asset Grid tap Lightning > On Send Address Screen header you should see Lightning icon and title should be Lightning

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
- [ ] Test Swap All

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

##  MEXAS/DEPIX Stablecoins
- [ ] Settings > Manage Assets > Add More Assets. Verify Mexas is available to add. Add and verify it is not on Home Screen and Send/Receive Grids
- [ ] Test Send and Receive from external wallet successfully. Verify txs show in tx history for Mexas


##  MARKETPLACE
- [ ] Test Meld flow
- [ ] Test Beaver Bitcoin shows if Region is CA
- [ ] Test Pocket Bitcoin shows if Region is Europe (not all but most EU countries)


## VPN + BAD/NO NETWORK CONDITIONS
- [ ] Test with a VPN on - some external endpoints have had issues with endpoints. 
    - Sideshift (USDt-Tether and Eth swaps) block US endpoints
- [ ] Test with bad network and no network
