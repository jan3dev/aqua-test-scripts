The following must be done on iOS and Android:

### Create Wallet
- [ ] Load up a fresh installation of the wallet

- [ ] Click on the terms of service and confirm it opens in a webview

- [ ] Click on create new wallet and confirm that a new wallet is created

- [ ] Go to Setting>View Seedphrase and verify that seed is shown

- [ ] Take a screenshot and confirm that a warning is shown

- [ ] Kill the app and restart and confirm that the backup screen is shown

### Backup Wallet
The backup wallet screen will only show for a new wallet that has at least one transaction. It will not show if you restore a wallet.

- [ ] Click on start backup > continue

- [ ] click on 4 wrong words and confirm and error screen is shown

- [ ] click retry and enter the 4 correct words and confirm that the user is taking to the home screen

### Restore Wallet
- [ ] Deposit a small amount of money into the wallet and turn on dark mode and delete the wallet. 

- [ ] Restart app and go through the restore workflow

- [ ] As words are being entered, confirm that the prompts are working

- [ ] Enter the same seed as last time (the screenshot taken above) but change the last word. Confirm that an error message is shown.

- [ ] Enter the same seed as last time (the screenshot taken above) but change one of the words to an invalid word. Confirm that an error message is shown.

- [ ] Enter the correct seed and confirm that the wallet is restored with the balance shown. Confirm that settings like darkmode are all reset from before

- [ ] Restore should be performed with a few different wallets to see how transaction fetching and balance update perform:
  - [ ] Minimal wallet with only a few LBTC txs
  - [ ] Wallet with other Liquid assets such as EURx
  - [ ] Power user wallet with lots of txs across different assets
