# GlobalProtect Smart Card Client Certificate Workaround

This guide provides a workaround for environments using Palo Alto GlobalProtect VPN and YubiKeys (or other smart cards) where the wrong client certificate is automatically selected.

## 🧩 Problem

When a smart card certificate includes the `Client Authentication` usage, GlobalProtect may select it incorrectly — breaking VPN access, even if the certificate is intended for Kerberos or RDP logon. However, removing Client Auth entirely breaks those other workflows.

## 💡 Solution

This step-by-step guide walks you through duplicating your existing smart card certificate template and:
- Removing the `Client Authentication` usage
- Adding `PKInit Kerberos` and `Remote Desktop` OIDs
- Issuing the new template alongside the original

## 📄 Included

- `Palo Alto Smart Card Client Auth Workaround.pdf`: Full step-by-step instructions with screenshots

## 🛠 Requirements

- Active Directory Certificate Services (ADCS)
- Permission to create/edit templates
- A working YubiKey or other PIV-compatible smart card device

## 🧪 Disclaimer

This workaround is provided as-is based on real-world troubleshooting. Use at your own discretion. Tested in a Windows AD environment with GlobalProtect and YubiKey.

---

> Authored by [Neil](https://github.com/neilfx1)
