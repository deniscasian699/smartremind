<div align="center">

# 🔐 Security Policy — SmartRemind

</div>

---

## Supported Versions

| Version | Supported |
|---|:---:|
| Latest (Google Play) | ✅ Active |
| Previous versions | ❌ No support |

Always use the latest version of SmartRemind available on Google Play to
ensure you have the most recent security fixes and improvements.

---

## Reporting a Vulnerability

If you discover a security vulnerability in SmartRemind, please report it
**responsibly** and **privately:**

> ⚠️ **Do not open a public GitHub issue for security vulnerabilities.**
> This could expose users before a fix is available.

### How to Report

1. Send an email to **[support@rdcapps.com](mailto:support@rdcapps.com)**
   with the subject line: `[SECURITY] SmartRemind Vulnerability Report`
2. Include in your report:
   - A clear description of the vulnerability
   - Steps to reproduce the issue
   - Potential impact assessment
   - Your suggested fix (if any)
   - Your Android version and SmartRemind version

### Response Timeline

| Step | Timeline |
|---|---|
| Acknowledgement | Within 72 hours |
| Assessment | Within 7 days |
| Fix release | Depends on severity |

We appreciate responsible disclosure and will credit researchers who help
keep SmartRemind secure (with their permission).

---

## Scope

| In Scope ✅ | Out of Scope ❌ |
|---|---|
| SmartRemind Android app | Google AdMob / UMP infrastructure |
| In-app purchase flows | Google Play / RevenueCat infrastructure |
| Widget security | Third-party advertiser websites |
| Notification handling | Physical device attacks |

---

## Known Security Practices

- ✅ All network requests use **HTTPS** encryption
- ✅ No plaintext credentials stored
- ✅ Advertising requests gated by Google UMP privacy requirements
- ✅ Eligible ad-removal purchases disable all ad formats
- ✅ Reminder and habit content is not sent to advertising services
- ✅ All preferences stored locally using Android SharedPreferences
- ✅ Purchase verification handled by RevenueCat (server-side)

---

*Thank you for helping keep SmartRemind and its users safe. 🌤️*
