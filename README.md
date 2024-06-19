# Getting Started
To begin testing, please refer to the detailed guidelines above. This guide covers everything you need to understand the testing process flow ensuring you have all necessary information at your fingertips.

# Testing Flow Overview
### L1. Smoke Test
A smoke test is a preliminary test to check the basic functionality of the application. It's a quick run-through to ensure that the critical features of the app are working as expected.

```https://github.com/jan3dev/aqua-test-scripts/blob/main/smoke_test.md```

### L2. Full Regression Test using scripts
This is a suite of tests that drills down into every feature and performs a thorough and comprehensive testing of the software. It covers a wide range of functionalities, including all edge cases possible (TODO).

```https://github.com/jan3dev/aqua-test-scripts/tree/main/full_regression_tests```

### L3. Full Regression Test with detail step by step
This involves a meticulous step-by-step verification of the application's functionalities to ensure thorough testing coverage.

| Test Case ID | Test Case Description | Test Steps                  | Expected Result          | Observed Results        | Actual Result (Android/ios) | Suggestions                |
|--------------|-----------------------|-----------------------------|--------------------------|-------------------------|--------------------------|----------------------------|


## How to Access Beta Versions ❓
Step-by-step instructions for accessing beta versions on iOS and Android, ensuring you're always on the cutting edge.
### For iOS Users
iOS is known for being more rigorous in its beta testing process. To access the beta version on iOS, you need a TestFlight invite.

 👀 TestFlight is Apple's platform that allows developers to distribute beta versions of their apps to selected testers. https://developer.apple.com/testflight/

**Steps for iOS Beta Access:**
1. **TestFlight Invite**:
You should have received an invite. Open the TestFlight app and accept the invitation.
2. **Install App**:
Download and install the beta version from TestFlight.

### For Android Users
For Android, you simply need to sign into the Play Store with your Jan3 email or ensure that your email account has been added as a tester.

**Steps for Android Beta Access:**
1. **Play Store Login:**
Sign into the Play Store using your Jan3 email address or your email account has been included as a tester.
2. **Join Beta Program:**
Go to the app’s page on the Play Store and join the beta program.
3. **Install App:**
Download and install the beta version.

# Testing on Testnet and Mainnet
## Testnet Testing 🛠️
Testnet is a safe environment for testing without any real financial impact. Here's how to get started:

### **Steps to Test on Testnet:**
1. Ensure you have version 0.2.0 of the app installed.
2. Tap the settings header five times to unlock experimental features.
3. Enable Testnet from the experimental features menu.
4. Close and reopen the app.
5. Look for the Bitcoin Testnet price—it confirms you're in Testnet!

By following these steps, you can confirm that you are testing in a safe environment without any real financial implication.  Perfect for trying new features!

### Useful Links for Testnet Testing 🌐
- https://liquidtestnet.com/faucet
- https://bitcoinfaucet.uo1.net/send.php
- https://faucet.triangleplatform.com/bitcoin/testnet

**Note:** Some functionalities do not support Testnet:
- Sideshift (USDT Eth + Tron swaps)
- Swap BTC <> LBTC (LBTC <> USDt swaps are available on Testnet)

## Mainnet Testing 🚀
Mainnet is where real transactions happen! Here’s what you need to know:

### Why Test on Mainnet Before Release? 
- **Real-World Readiness:** Ensures your app performs reliably under live transaction conditions.
  
  #### 💡 When Mainnet Testing Might Make Sense:
  - Identifying critical issues that may only manifest under real user and transaction conditions.
  - Gathering valuable real-world data and user feedback that can't be fully replicated in testnets.
  - Verifying that all features operate seamlessly in a live, dynamic network environment
    
- **Early Risk Mitigation:** Prevents potential setbacks by catching and resolving issues pre-release.
- **Balancing Innovation with Responsibility:** Innovate cautiously to respect network stability and security.

### Now that you're on Mainnet/Testnet, Check This Out! 🔍

## Assets involved
- **Bitcoin**
- **Usdt (en liquid, tron, ethereum)**
- **Lightning**
- **Liquid bitcoin**
## Test data
**COMING SOON 🚀**
## 🔧 Tools and apps you need to install to start testing.
- **Green:** Supports various seed options. You can seamlessly send and receive LBTC and BTC between different wallets on both Testnet and Mainnet environments.
- **Sideswap:** Shares the same seed as Aqua for easy continuity and testing.
- **Trust:** Enables transactions with USDt on Ethereum and Tron networks.
#### 🔗 Explore a Web Wallet Demo:
```https://demo.lnbits.com/```
## Must-Knows 🌟
### **Way to setup an LNURLp (including lightning address) and LNURLw server for testing**
  1. Create an account at ```LNBits.com```
  2. Launch and instance and pay the 21 sats fee
  3. Install both LNURLp and LNURLw extensions
### **Reporting Bugs in Version 0.2.0: Where Can I Report Them? 🐞**

If you spot any bugs in version 0.2.0 of Aqua.
```https://github.com/jan3dev/aqua-dev/issues```
### **Accessing Older APKs for Android: How Can I Get Them?** 

Visit our public repository on GitHub to download previous releases  ```https://github.com/AquaWallet/aqua-wallet/releases```
### **Why do I only see the bip21 address in the QR code when setting an amount? How can I ensure it's generated correctly?**

In Aqua, we've streamlined the process by displaying the bip21 address exclusively within the QR code when you enter an amount in "Receive." To ensure it's generated correctly, simply scan the QR code with your device or use a reliable QR code reader.

### **Third-Party Apps involves:**
  - sideswap.io
  - sideshift.ai

### 🚀 With everything ready... Let's test it out!


### After testing... 
## 📊 General Report
The general report plays a crucial role in summarizing and effectively communicating testing outcomes. It documents tested features, executed test cases, and encountered issues comprehensively. Its primary purpose is to provide a clear and concise overview of the product's testing status.

|**General Information**  |**Details**          |
|-------------------------|---------------------|
| Build Date          | _[Date]_             |
| Version Number      | _[Version Number]_    |
| Platform            | _[Android]_             |
| Build Type          | _[Debug/Release]_     |
| Test Device         | _[Device Name]_       |
| Testing Responsible | _[Responsible Person's Name]_ |



| **Summary of Tests Conducted**            |**Details**                               |
|-------------------------|---------------------|
| Features added with the build         | _[List of new features added]_         |
| Tested Functionalities                | _[List of tested functionalities]_     |
| Test Cases Executed                   | _[Total number of test cases executed]_|



|**Issues Found**                          |**Details**                                   |
|-------------------------|---------------------|
| Total Issues Found                    | _[Total number of issues found]_       |
| Issues Found                          | _[Detailed list of issues encountered during testing, including error number, description, severity, and current status]_ |



|**Conclusions and Recommendations**       |**Details**                                     |
|-------------------------|---------------------|
| Summary of Test Results               | _[Summary of test results]_            |
| Quality Assessment                    | _[Conclusion regarding the version's quality]_ |
| Recommendations                       | _[Recommendations for future improvements]_ |




