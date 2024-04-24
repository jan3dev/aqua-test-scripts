TODO: This was copied from the smoke test to start the folder - needs to be filled out with full functionality.

## SEND
### ADDRESS - QRSCANNER + TEXT FIELD ENTRY
- [ ] Test scanning valid QR codes for all available assets
    - [ ] Bitcoin
      - [ ] TODO: Add all variations of Bitcoin addresses
    - [ ] Liquid
      - [ ] TODO: Add all variations of Liquid addresses, confidential and unconfidential
    - [ ] Lighting Invoice
      - [ ] TODO: Add all variations of lightning invoices
      - [ ] Error State: Expired invoices show prompt
      - [ ] Error State: No amount invoices show prompt

- [ ] Bip21
    - [ ] Liquid address that's not LBTC and has a valid assetId goes to proper asset (eg, USDt with assetId goes to Send USDt asset page)
    - [ ] BTC with Lightning fallback goes to Lightning Send (will have option to choose lightning or btc in the future)
    - [ ] Scan bip21 with lightning fallback but user has 0 second layer balance, should resolve to BTC automatically


- [ ] Lightning Address
    - [ ] Test from a variety of servers, large and small. A list to start: Blink, Coinos, Alby, Strike, Wallet of Satoshi
    - [ ] When the lightning address is entered on the Send Address Screen, the Continue button should enable once text passing a basic email regex is entered. This has not entered the lightning address resolution flow yet, the initial validation is just a basic email regex.

- [ ] LNURL

The above are general address validation steps for the QR scanner on any screen. 
Below are steps to validate scanning QRs on asset specific screens

- [ ] Compatible/Incompatible Assets
    - [ ] If a QR or text address input is entered on an asset specific screen, we show an invalid asset if the asset doesn't match.
    - [ ] There are exceptions where lightning and lbtc are considered "compatible" assets and should not show an error
    - [ ] USDt Liquid, Tron and Ethereum addresses are all "compatible" and should switch to that version of a USDt send.
     
### AMOUNT (All Assets)
- [ ] Verify when tap Send All button, amount field is still editable and de-activates Send All button when edited. Verify correct amount shows in Review Screen
 
### BITCOIN
- [ ] Regular Send
- [ ] Verify fee rates show and change when tapped - also verify this is the actual rate in the tx
- [ ] Send All
- [ ] Fiat-denominated
- [ ] Verify tx shows up in tx history
- [ ] Error State: Verify amount over balance shows error

### LBTC
- [ ] Regular Send
- [ ] Send All
- [ ] Fiat-denominated
- [ ] Verify tx shows up in tx history
- [ ] Error State: Verify amount over balance shows error

### LIGHTNING (Boltz)
- [ ] Send various wallets
- [ ] Send various Lightning Address
- [ ] Send Aqua-to-Aqua (converts to LBTC send)
    - [ ] Verify when scan an Aqua-to-Aqua LN QR that it scans successfully and populates a liquid address and an amount in send flow
    - [ ] Verify sending to address
    - [ ] On receive side, there is no success screen (https://github.com/jan3dev/aqua-dev/issues/755), but verify receive
- [ ] Verify shows up in Tx Detail
- [ ] Edge Case: Scan an invoice that already has a swap initiated

### BOLTZ SWAP REFUNDS
TIMELOCKED REFUNDS: The boltz submarine swap can fail for a number of reasons, mainly lightning liquidity or routing issues. These happen more often with smalle nodes. If a swap fails, you will still see the tx success screen as the lbtc sats were sent successfully. However, in the tx detail screen for that lbtc send the boltz section will show failed. Because of the timelock on the refund half of the script, users must wait around 48 hours to claim a refund. In Bravo release this will be done automatically with the swap checker, and you will see a new transaction for those sats. The swap checker runs on each new app start.

COOPERATIVE REFUNDS: When taproot swaps are implemented, cooperative swaps should happen near instantanesouly once a failure state comes back from boltz.


### USDT
- [ ] Regular Send - Liquid USDt
    - [ ] NOTE: Redeposits don’t show up in tx history due to gdk
- [ ] Sideshift
    - [ ] Verify Sideshift order shows up in order history (currently in history button on USDT tx history screen), even if pending
    - [ ] Verify Send (no testnet unfortunately)
    - [ ] Error State: If not in an allowed country, verify error message (US is not an allowed country)

### OTHER ASSETS (EURx, JPY, etc)
- [ ] Regular Send on any other asset
- [ ] Send All
- [ ] Verify shows up in Tx Detail
- [ ] Error State: Verify amount over balance shows error

### REVIEW SCREEN - ALL ASSETS
- [ ] Verify amount and address are correct
- [ ] Verify network fees are correct (cross check with blockchain explorer)
- [ ] Sideshift: Verify shift id and fee display
- [ ] Boltz: Verify fee displays

### SUCCESS SCREEN - ALL ASSETS
- [ ] Verify amount, network fee, tx id, time in utc, date
