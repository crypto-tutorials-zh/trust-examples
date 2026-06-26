# Seed Phrase & Mnemonic Security Guide

# Seed Phrase & Mnemonic Security Guide

## Overview
A curated reference for understanding BIP39 mnemonic seed phrases, storage strategies, and recovery procedures across major cryptocurrency wallets.

## Seed Phrase Standards

| Standard | Word Count | Entropy Bits | Use Case | Security |
|----------|-----------|-------------|----------|----------|
| BIP39 | 12 words | 128 bits | Mobile wallets, exchanges | Standard, widely supported |
| BIP39 | 24 words | 256 bits | Hardware wallets, long-term | Maximum entropy, preferred for high-value |

## Storage Best Practices

### ✓ Recommended
- **Metal wallet backup** (fireproof, waterproof)
- **Offline paper wallet** (air-gapped, sealed container)
- **Geographically distributed copies** (separate safe locations)
- **Multi-signature setup** (requires N-of-M keys to recover)
- **Encrypted digital backup** (password-protected, encrypted USB)

### ✗ Avoid
- Screenshots or digital photos
- Cloud storage (Google Drive, Dropbox, iCloud)
- Email or messaging apps
- Unencrypted notes or documents
- Single physical location

## Recovery Process (Trust Wallet Example)

1. Open Trust Wallet → Tap **Settings**
2. Select **Wallets** → Choose wallet
3. Tap **Show Recovery Phrase** → Authenticate
4. **Write down all 12/24 words in exact order**
5. Verify by re-entering during setup
6. Store securely offline

## Common Scam Vectors

| Scam Type | Red Flags | Prevention |
|-----------|-----------|------------|
| "Help recover wallet" support | Unsolicited DMs asking for seed phrase | Never share seed phrase with anyone |
| Fake wallet recovery tools | Links claiming to "restore" wallet | Only use official wallet apps |
| Phishing sites | URLs mimicking real wallets | Bookmark official sites, verify domains |
| QR code replacement | Fake recovery codes | Manual entry is safer than QR scanning |

## Wallet Comparison: Seed Phrase Support

| Wallet | Supports 12-word | Supports 24-word | Can view seed | BIP39 Standard |
|--------|-----------------|-----------------|---------------|----------------|
| Trust Wallet | ✓ | ✓ | ✓ (in-app) | ✓ |
| MetaMask | ✓ | ✓ | ✓ (settings) | ✓ |
| Ledger Hardware | ✓ | ✓ | ✗ (offline only) | ✓ |
| Trezor Hardware | ✓ | ✓ | ✗ (offline only) | ✓ |
| Exodus | ✓ | ✗ | ✓ | ✓ |

## Key Takeaways

- **BIP39 standard** is the industry backbone for mnemonic seed phrases
- **12 words = 128-bit entropy** (sufficient for most users)
- **24 words = 256-bit entropy** (recommended for large holdings)
- **Never digitize or share** recovery phrases
- **Multiple offline backups** reduce single-point-of-failure risk
- **Test recovery procedure** on a new device before relying on it

## References
- BIP39 Standard: https://github.com/trezor/python-mnemonic
- Trust Wallet Docs: https://trustwallet.com/security
- Hardware Wallet Recovery: Ledger/Trezor official guides

## Reference

[https://trendkoin.com](https://trendkoin.com/wallet/trust-wallet-seed-phrase)
