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
- [ ] Bip21
    - [ ] Liquid non-LBTC with assetId goes to proper asset
    - [ ] BTC with Lightning fallback goes to Lightning Send
- [ ] Lightning Address
- [ ] LNURL
### BITCOIN
- [ ] Regular Send
- [ ] Verify fee rates show and change when tapped
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
- [ ] Send Aqua-to-Aqua (converts to LBTC send)
- [ ] Verify shows up in Tx Detail

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

### LBTC
- [ ] If amount is entered, the text displayed and copy button don’t include the bip21, but Share and QR include the full bip21 with AMOUNT and ASSETID
    - [ ] Also test fiat-demoninated is converted to lbtc in bip21
- [ ] Switch between LBTC/Lightning is smooth and resets state

### LIGHTNING
- [ ] Invoice generated
- [ ] Generated Invoice has routingHints from Boltz (for aqua-to-aqua send)
- [ ] Success screen shows upon invoice payment

### USDT
- [ ] Switch between networks is smooth and resets state
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
- [ ] Test Peg out


## TX HISTORY/DETAIL SCREENS



## ## SETTINGS
- [ ] Invite others to AQUA
- [ ] Get Help
- [ ] Language
- [ ] Region (does nothing right now)
- [ ] Biometric Auth
- [ ] Dark/Light/Botev Mode
- [ ] Default Explorer
- [ ] Manage Assets - Add and verify they show with balances
- [ ] View Seed Phrase
- [ ] Bitcoin Chip - ?
- [ ] TOS/Privacy/Social Links



##  MARKETPLACE
- [ ] Test Meld flow