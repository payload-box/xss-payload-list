# 🛡️ Ultimate XSS Payload List & Learning Hub

![Maintenance](https://img.shields.io/maintenance/yes/2026)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Contributors](https://img.shields.io/badge/contributors-welcome-orange.svg)

## 🎯 About The Project

This project aims to provide a comprehensive resource for understanding and testing Cross-Site Scripting (XSS) vulnerabilities, one of the **OWASP Top 10** security risks. It is designed to be a useful resource for security researchers, penetration testers, and developers.

**Goal:** To explain XSS vulnerabilities from the OWASP Top 10 lists and provide a beneficial study for the security world.

<img src="https://github.com/payload-box/xss-payload-list/blob/main/Docs/xss-payload-list-ismailtasdelen.jpeg">

## 📂 Project Structure

- **`Payloads/`**: A vast collection of XSS payloads categorized by type and use case.
  - **`Basic/`**: Fundamental payloads for testing standard injection points.
  - **`Bypass/`**: Techniques to bypass WAFs and filters (Encoding, Obfuscation).
  - **`Polyglots/`**: "Write once, run everywhere" payloads that work in multiple contexts.
  - **`BurpIntruder/`**: Optimized wordlists for fuzzing with Burp Suite Intruder.
  - **`Frameworks/`**: Framework-specific payloads (Angular, Vue, React, Svelte, jQuery).
  - **`Blind/`**: Payloads for Blind XSS scenarios (XSS Hunter).
  - **`CSP-Bypass/`**: Techniques to bypass Content Security Policy.
  - **`WAF-Bypass/`**: Payloads tailored for specific WAFs (Cloudflare, ModSecurity).
- **`Docs/`**: Educational resources to learn about XSS mechanics and prevention.
- **[Cheatsheet](Cheatsheet.md)**: A quick reference guide.

## 📚 What is XSS?

Cross-Site Scripting (XSS) occurs when an application includes untrusted data in a new web page without proper validation or escaping.

### Types of XSS

1. **Reflected XSS**: The malicious script comes from the current HTTP request.
2. **Stored XSS**: The malicious script is stored in the database and served to victims later.
3. **DOM XSS**: The vulnerability exists in client-side code rather than server-side code.

## 🚀 Usage

Navigate to the `Payloads` directory and choose the category that fits your testing scenario.
For educational content, check the `Docs` folder.

### For Burp Suite Intruder

Use the lists in `Payloads/BurpIntruder` for automated fuzzing.

## ⚠️ Disclaimer

This repository is for **educational and authorized testing purposes only**. The author is not responsible for any misuse of the information or code provided herein. Always obtain proper authorization before testing any system.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
