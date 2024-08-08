The following must be done on iOS and Android:

### Invite Others to Aqua
- [ ] Click on the button and make sure the share option show up

### Get Help
- [ ] Click on get help>zendesk and confirm that the zendesk website opens up as a webview


### Language
- [ ] Click on a language other than english and confirm that it switches

- [ ] Click on the header 5 times to see if hidden langugages show

### Region
- [ ] Select a region and confirm that its reflected in the marketplace tab

- [ ] Change the region and confirm that its reflected in the marketplace tab

### Biometric Authentication
- [ ] Confirm that the biometric authetication option does not show for a phone without biometrics available

- [ ] Turn off biometrics on the phone and confirm that the option is disabled in the aqua wallet

Turn on biometric and confirm that it executes the biometric auth and and is enabled. 
- [ ] Kill the app and confirm that it asks for biometric auth
- [ ] Go to the delete wallet and confirm that it asks for biometric auth
- [ ] Go to the view seed words option and confirm that it asks for biometric auth

Turn off biometric and confirm that it executes the biometric auth and and is enabled. 
- [ ] Kill the app and confirm that it does not ask for biometric auth
- [ ] Go to the delete wallet and confirm that it does not ask for biometric auth
- [ ] Go to the view seed words option and confirm that it does not ask for biometric auth

Enable biometric, kill the app and reopen, when biometric auth comes up, intentionally fail it and autheticate via phone password/pin

### Dark Mode
- [ ] turn on an off dark mode and confirm that color changes

### Botev Mode
- [ ] Turn on and off botev mode and confirm that the color changes

Turn on botev mode from light mode and confirm that it switches the light/dark mode toggle to dark and keeps it disabled while in botev mode

### Default Block Explorer
- [ ] Change the default block explorer and go to a transaction detail screen and click on the link to open the BE and confirm that the change was picked up

### Manage Assets
- [ ] Remove USDT and confirm that it disappears from the wallet asset list, the send and receive screens and the swap options.
      
- [ ] Remove USDT and check the Send screens for Bitcoin and LBTC, and confirm that the 'USDt Internal Send' button is gone from the Send > LBTC screen.
      
- [ ] Add USDt back to managed assets and confirm the 'USDt Internal Send' button reappears on the Send > LBTC screen.

- [ ] Add a non default asset (like pegX) and confirm that it appears in the wallet asset list and the send and receieve screens.

- [ ] Change other of the assets and confirm that its reflected in the wallet asset list screen

### View Seed Phrase
(covered above)

### Bitcoin Chip
TBD

### Delete Wallet
(covered in the onboarding test suite)

### Bottom Links
Click on the following links and make sure the approporiate website opens
- terms of service
- privacy policy
- website
- twitter
- instagram
