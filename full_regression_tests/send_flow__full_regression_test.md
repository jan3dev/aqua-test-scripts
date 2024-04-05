TODO: This was copied from the smoke test to start the folder - needs to be filled out with full functionality.

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
- [ ] Send various Lightning Address
- [ ] Send Aqua-to-Aqua (converts to LBTC send)
    - [ ] Verify when scan an Aqua-to-Aqua LN QR that it scans successfully and populates a liquid address and an amount in send flow
    - [ ] Verify sending to address
    - [ ] On receive side, there is no success screen (https://github.com/jan3dev/aqua-dev/issues/755), but verify receive
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
