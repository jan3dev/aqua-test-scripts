## RECEIVE FLOW

### ASSETS
- [ ] Verify the default assets plus all assets added in Settings > Managed Assets are display in Receive Asset Grid


### AMOUNT ENTRY - All assets
- [ ] Verify text entry is restricted to numbers and a single decimal
- [ ] Verify decimals are capped at the precision of the asset (most have a precision of 8, so should be capped at 8 decimals)


### BITCOIN
- [ ] Displays valid, unused Bitcoin address in text that's copyable. Verify correct address is copied.
- [ ] Displays same address in QR code
- [ ] Enter amount allows entry in sats or fiat with conversion
- [ ] Enter amount will create a bip21 for the Share button only. The text display and QR will only show the base address
- [ ] Back button then re-enter Receive Bitcoin Screen and verify that new address displays (gdk rotates addresses) and verify that it's correctly copied.

### LBTC
- [ ] Same steps as Bitcoin, except verify that correct assetId shows in bip21 on Share button
  
### LIGHTNING
- [ ] Verify switch between tabs for LBTC and Lightning resets state for asset (we might want to change this in future to save state, especially for boltz which requires an api call)
- [ ] Verify service fee from Boltz displays
- [ ] Verify enter amount in sats or fiat with conversion
- [ ] Verify tap "Generate Invoice" button shows spinner and resolves to a return invoice from boltz
- [ ] Success Screen: This is unique to lightning on receive page for now. If the generated invoice is paid, verify a success screen displays with amount received
- [ ] Error State: Verify error shows when enter an amount above or below boltz max/min
- [ ] NEED TO test claims with a variety of delays to mimic real world usage
  - [ ] Create invoice, background app for > 15min, pay invoice from another app, foreground app and verify that claim function runs and receive is completed.
  - [ ] Create invoice, close app. Pay invoice from another app. Open Aqua and verify that claim function runs and receive is completed.


### USDT
- [ ] Same steps as LBTC for Liquid USDt

- [ ] Tron and Ethereum
  - [ ] Verify switch between tabs resets state for asset (we might want to change this in future to save state, especially for boltz which requires an api call)
  - [ ] Verify on enter screen that a spinner displays while sideshift order call returns
  - [ ] Verify on order response that receive address, QR, expiry, min/max, fee breakdown and shiftId display
  - [ ] Verify "Share" shares address only
  - [ ] Error State: Verify if in a country that's blocked (US is one) then an error displays instead of response

### OTHER LIQUID ASSETS (EURx, JPY, etc)
- [ ] Same steps as LBTC for Liquid USDt
