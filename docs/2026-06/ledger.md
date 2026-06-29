# Hardware Wallet Security Evaluation Framework

# Hardware Wallet Security Evaluation Framework

## Security Dimensions Checklist

Use this framework to evaluate hardware wallets (Ledger, Trezor, etc.):

### Chip-Level Protection
- [ ] Secure element (CC EAL5+ or equivalent certified)
- [ ] Physical tamper detection and response
- [ ] Side-channel attack resistance (power analysis, timing)
- [ ] Fault injection countermeasures
- [ ] Cryptographic acceleration (ECDSA, EdDSA native)

### Key Management
- [ ] Private keys never leave secure element
- [ ] Hardware-enforced transaction approval (button/screen)
- [ ] PIN/passphrase enforcement before signing
- [ ] Recovery seed handling (offline, entropy source)
- [ ] Firmware signature verification

### Attack Surface
- [ ] USB communication encryption
- [ ] Firmware update authentication
- [ ] Third-party recovery/seed recovery service (trust model, privacy)
- [ ] Firmware open-source audit trail
- [ ] Known CVE history and patch cadence

### Operational Security
- [ ] Merchant/vendor lockout mechanisms
- [ ] Multi-signature support
- [ ] Custom derivation path support
- [ ] Reproducible build certification
- [ ] Independent security audits published

## Ledger Nano S/X/Stax Security Profile

| Feature | Level | Notes |
|---------|-------|-------|
| Secure Element | CC EAL5+ certified | ST31H320 / ST33H298 |
| Tamper Detection | Hardware | Physical attack response |
| Side-Channel Protection | Built-in | ECDSA hardening |
| Firmware Updates | Signed & encrypted | Recovery required |
| Recovery Service | Optional (Ledger Recover) | Controversial: trusts 3 custodians |
| Open Source | Partial | App SDK open, OS closed |
| Audit History | Published (rare) | Security audits available online |
| Multi-sig Support | Yes | With third-party wallets |

## Trade-offs to Evaluate

**Ledger strengths:**
- Certified secure element, proven physical defense
- Wide app ecosystem (200+ coins)
- Large user base, frequent audits

**Ledger concerns:**
- Closed-source OS (BOLOS)
- Ledger Recover service requires sharing encrypted seed with 3 custodians
- Firmware update mechanism requires vendor trust
- Optional but persistent recovery service

## Decision Matrix

Choose based on your threat model:

| Priority | Recommendation |
|----------|----------------|
| Maximum security, self-custody only | Trezor Model T (open source TREZOR OS) |
| Certified EAL5+, wide support, accept Recover risk | Ledger Nano X |
| Air-gap + no USB, maximum isolation | Blockstream Jade or Coldcard |
| Multi-sig + institutional audit trail | Ledger + hardware multisig orchestration |

## References
- CC EAL5+ certification: Industry standard for secure elements
- Ledger Recover controversy: Trade-off between convenience and seed custody
- TREZOR open-source advantage: Full firmware reproducibility

## Reference

[https://trendkoin.com](https://trendkoin.com/wallet/ledger-security)
