# Privacy Policy for VaultFin

**Last Updated:** January 30, 2026

## Introduction

VaultFin ("the App") is a privacy-first personal finance application developed by VaultFin ("we", "us", or "our"). This Privacy Policy explains how we handle information when you use our Android application.

**Our Core Principle:** Your financial data stays on your device. We do not collect, store, or have access to your personal or financial information.

## Information Collection and Storage

### What Data is Stored

The App stores the following data **locally on your device only**:

- **Financial Transactions:** Transaction data synced from your bank accounts via SimpleFIN, including amounts, descriptions, dates, and categories
- **Account Information:** Bank account names, types, and balances
- **User Preferences:** App settings, custom categorization rules, and display preferences
- **SimpleFIN Access Token:** Your SimpleFIN authentication token (stored securely in Android Keystore)

### How Data is Stored

- All financial data is stored in a local SQLite database encrypted with SQLCipher using **AES-256 bit encryption**
- Your decryption key is managed via the Android Keystore system, ensuring that data cannot be accessed without your device credentials or biometric authentication
- Data never leaves your device except when you initiate a bank sync through SimpleFIN

### Internet Usage

Our application requires Internet access **solely** for the purpose of communicating directly with the SimpleFIN API to retrieve your financial data. No data is transmitted to VaultFin or any other third-party servers. All processing happens on your device.

The App operates locally and only connects to the internet when you explicitly request a bank synchronization through SimpleFIN.

### Network Communication

The App makes no network connections to VaultFin servers because we do not operate any servers. The only network communication is:

1. **SimpleFIN API** - Direct HTTPS connection to SimpleFIN servers when you initiate a bank sync
2. **Google Play Billing** - Standard Google Play purchase verification (handled by Google's SDK)

### What We Do NOT Collect

We do not collect, transmit, or have access to:

- Personal identification information (name, email, phone number)
- Location data
- Device identifiers or advertising IDs
- Usage analytics or behavioral data
- Crash reports or diagnostics
- Any financial data from your device

**The App contains no analytics SDKs, advertising frameworks, or tracking mechanisms.**

## Device Permissions

The App requests the following Android permissions:

- **Internet:** Used exclusively for direct communication with the SimpleFIN API when you initiate a bank sync. No other network communication occurs.
- **Biometrics:** Used locally via Android BiometricPrompt to unlock the application. Biometric data never leaves the device's Secure Enclave/Keystore and is never accessible to us.
- **Camera (optional):** Used only if you choose to scan a SimpleFIN QR code for setup. Images are processed locally and immediately discarded.

## Third-Party Services

### SimpleFIN (User-Directed Service)

The App acts as a client interface for the SimpleFIN Bridge service (https://www.simplefin.org/). **Your relationship with SimpleFIN is separate and direct:**

- **User-Initiated:** Bank sync only occurs when you explicitly request it
- **Direct Connection:** Your device connects directly to SimpleFIN's servers; we have no intermediary server and do not see or process your data
- **Your Account:** You create and manage your SimpleFIN account separately; you pay SimpleFIN directly for their service
- **Your Credentials:** We never have access to your bank login credentials. SimpleFIN handles authentication directly with your financial institutions.
- **Token Storage:** Your SimpleFIN access token is stored securely in Android Keystore on your device

**Important:** Your relationship with SimpleFIN is governed by their separate Terms of Service and Privacy Policy. VaultFin is not responsible for SimpleFIN's data handling, availability, or data accuracy. We encourage you to review SimpleFIN's privacy policy at their website.

### Google Play Billing

For in-app purchases, we use Google Play Billing:

- Purchase transactions are processed by Google
- We receive only purchase verification tokens, not payment details
- Google's privacy policy governs their handling of payment information

### Technical Log Data

In the event of an application error, the App does not automatically transmit crash reports to us. If the Android Operating System collects crash data (tombstones), this is governed by your device settings and Google's Privacy Policy.

## Data Security

We implement the following security measures:

- **Encryption at Rest:** All financial data encrypted with SQLCipher (AES-256)
- **Secure Key Storage:** Encryption keys protected by Android Keystore
- **Biometric Protection:** Optional biometric authentication to access the app
- **Screen Security:** FLAG_SECURE prevents screenshots of sensitive screens
- **No Network Transmission:** Data is never transmitted to our servers (we have none)

## Data Retention and Deletion

- **Your Control:** All data is stored locally on your device under your complete control
- **Deletion:** Uninstalling the App permanently deletes all stored data, including the encrypted SQLCipher database and all Keystore entries
- **User-Managed Backups:** You may choose to generate an encrypted full backup of your data (.localfin file). This file is generated locally on your device. You are responsible for storing this file securely (e.g., in your personal cloud storage or local file system). We do not transmit, store, or have access to your backup files or the encryption passwords you set for them.
- **Export:** You can export your categorization rules separately for portability

### Data Deletion Request

VaultFin does not create user accounts or store user data on our servers. Therefore, we do not possess any data to delete on your behalf.

**To permanently delete your data:**
1. Uninstall the VaultFin application from your Android device
2. This will remove the encrypted SQLCipher database and all Android Keystore entries associated with the App

For questions about data deletion, visit: https://reveille45.github.io/vaultfin-legal/

Or contact us at: vaultfin.app@gmail.com

## Children's Privacy

VaultFin is not directed at children under the age of 13. We do not knowingly collect or solicit personal data from anyone under the age of 13. If you are under 13, please do not use the Application. If you are a parent or guardian and believe your child has used the App, please note that uninstalling the App will remove all locally stored data.

## Your Rights

Since all data is stored locally on your device and we have no access to it:

- **Access:** You have full access to all your data within the App
- **Portability:** You can export your categorization rules at any time
- **Deletion:** Uninstall the App to delete all data permanently
- **No Data Requests Needed:** We cannot provide, modify, or delete your data because we don't have it

## Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will notify you of any changes by updating the "Last Updated" date at the top of this policy. We encourage you to review this Privacy Policy periodically.

## California Privacy Rights

If you are a California resident, you have specific rights under the California Consumer Privacy Act (CCPA). However, since we do not collect personal information on our servers, these rights are already inherently satisfied—there is no personal data for us to disclose, sell, or delete.

## International Users

The App processes all data locally on your device. No data is transferred internationally by us because no data is transferred to us at all. When you sync with SimpleFIN, data transmission is between your device and SimpleFIN's servers, governed by SimpleFIN's privacy policy.

## Contact Us

If you have questions about this Privacy Policy, please contact us at:

**Email:** vaultfin.app@gmail.com

**Privacy Policy:** https://reveille45.github.io/vaultfin-legal/

---

## Google Play Data Safety Form Guide

When completing the Google Play Console Data Safety section, use these answers:

### Data Collection

| Data Type | Collected? | Shared? | Details |
|-----------|------------|---------|---------|
| Financial info (Bank account) | **Yes** | No | Collected from SimpleFIN, stored locally only |
| Financial info (Purchase history) | **Yes** | No | Transaction data stored locally only |
| Personal info | No | No | — |
| Location | No | No | — |
| App activity | No | No | — |
| Device info | No | No | — |

### For "Financial Info" Responses:

- **Is this data collected, shared, or both?** Collected only
- **Is this data processed ephemerally?** No (stored in local database)
- **Is this data required for your app, or can users choose whether it's collected?** Required for core functionality
- **Why is this data collected?** App functionality (tracking personal finances)

### Security Practices

- **Data encrypted in transit:** Yes (HTTPS to SimpleFIN)
- **Data encrypted at rest:** Yes (SQLCipher AES-256)
- **Users can request data deletion:** Yes (uninstall removes all data)
- **Committed to Play Families Policy:** Not applicable (not a family app)

### Important Notes

- Even though data stays on the device, Google considers fetching data from SimpleFIN as "collection" by the app
- Specify in the detailed description that data is "stored locally on the user's device only"
- The app does NOT share data with any third parties for advertising, marketing, or analytics

---

*This privacy policy is provided for informational purposes. You should consult with a legal professional to ensure compliance with all applicable laws and regulations.*
