## USDt

- [ ] Settings > Manage Assets > Toggle off USDT. Check the places where USDt appears and ensure nothing unusual is present. 
    - We had a previous bug where there was a big grey box on the swap asset receive input when USDt was removed from manage assets
 
## Mexas (mx stablecoin)

- [ ] Settings > Manage Assets > Add More Assets. Verify Mexas is available to add. Add and verify it is not on Home Screen and Send/Receive Grids
- [ ] Settings > Region > Select Mexico. Verify that Home Screen shows Mexas by default.
- [ ] Settings > Manage Assets > Add More Assets. Remove Mexas. Verify it is removed from Home Screen. Close/Reopen and verify it is still removed
- [ ] Repeat changing region to Mexico so Mexas is auto-added to Home Screen. Change region to !Mexico. Verify Mexas is auto-removed from Home Screen
- [ ] Test Send and Receive from external wallet successfully. Verify txs show in tx history for Mexas
- [ ] Verify fiat conversion don't show or otherwise don't have any issues
- [ ] Verify asset symbol for mexas asset on receive amount input

## Other Assets 
- [ ] Verify asset symbol for stablecoins asset on receive amount input
