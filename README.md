# 🔐 Protecting API Keys & Passwords

A **beginner-friendly cybersecurity guide** created for **Cloud Native Ilorin**, focused on helping developers, students, and non-security professionals understand how to properly protect passwords and API keys in real-world applications.

This repository replaces traditional slide decks with a **clear, practical, and readable reference** that can be revisited anytime.

---

## 🎯 Purpose of This Guide

Many security breaches do **not** happen because of advanced hacking techniques.
They happen because:

* Passwords are weak or reused
* API keys are exposed in source code
* Secrets are pushed to public repositories

This guide explains **why these mistakes are dangerous** and **how to fix them using industry best practices**, explained in simple language.

---

## 👥 Target Audience

* Beginners in cybersecurity
* Software developers
* Cloud / DevOps beginners
* Students
* Anyone working with APIs, cloud services, or source code

No prior security knowledge is required.

---

## 📌 Key Concepts Covered

* What passwords and API keys are
* Why leaked secrets are dangerous
* Password best practices
* Password managers and MFA
* Secure handling of API keys
* Environment variables
* Principle of Least Privilege
* Key rotation

---

## 🔑 Understanding Passwords vs API Keys

### 🔑 Passwords

Passwords are **credentials used by humans** to prove identity.

They protect:

* Email accounts
* Social media
* Cloud dashboards
* Developer tools

If a password is compromised, attackers gain **direct access**.

---

### 🧩 API Keys

API keys are **credentials used by software applications** to access services.

They allow applications to:

* Read or write data
* Access cloud resources
* Make authenticated API requests

> If someone has your API key, the system assumes they are trusted.

API keys should be treated with the **same or higher security** as passwords.

---

## 🚨 Real-World Impact of Leaked Secrets

Leaked passwords or API keys can lead to:

* Data breaches
* Unauthorized cloud billing
* Account takeover
* Service disruption

Many major incidents happened **not because of hacking**, but because secrets were exposed publicly (e.g., on GitHub).

---

## 🔐 Password Best Practices

### ✅ Use Strong Passwords

* Minimum of **12 characters**
* Avoid names, birthdays, or common patterns
* Prefer long passphrases over short complex passwords

Example:

```
correct-horse-battery-staple
```

---

### 🔁 Avoid Password Reuse

Reusing passwords means:

* One breach compromises multiple accounts

Always use **unique passwords** for every service.

---

### 🗝️ Use a Password Manager

Password managers:

* Generate strong passwords
* Store them securely
* Prevent reuse

Recommended options:

* Bitwarden
* 1Password
* LastPass

Using a password manager is **more secure**, not less.

---

### 🔒 Enable Multi-Factor Authentication (MFA)

MFA adds an extra layer of protection:

* Something you know (password)
* Something you have (phone, authenticator app)

Authenticator apps are preferred over SMS.

---

## 🔐 API Key Security Best Practices

### ❌ What NOT to Do

Never store secrets directly in your code:

```js
const API_KEY = "sk-123456";
```

Never:

* Commit API keys to GitHub
* Share keys in screenshots
* Store keys in plain text files

Attackers actively scan public repositories for exposed secrets.

---

### ✅ Use Environment Variables

Environment variables allow secrets to be stored **outside the source code**.

Example:

```bash
export API_KEY="sk-123456"
```

Access in code:

```js
process.env.API_KEY
```

This ensures secrets are not included when code is shared or deployed.

---

### 🛡️ Principle of Least Privilege (PoLP)

Always restrict API keys to the **minimum permissions required**.

Examples:

* Read-only access instead of full access
* Limited scopes instead of admin privileges

If a key is leaked, the damage is minimized.

---

### 🔄 Key Rotation

Key rotation involves:

* Regularly replacing old keys
* Revoking unused or exposed keys

Benefits:

* Limits the lifespan of leaked keys
* Reduces long-term risk

---

## ✅ Key Takeaways

* Use password managers and MFA
* Treat API keys as sensitive credentials
* Never store secrets in source code
* Use environment variables
* Apply least privilege
* Rotate keys regularly

Security is not about perfection — it is about **good habits**.

---

## 📚 Additional Resources

* OWASP Top 10
* NIST Password Guidelines
* GitHub Secret Scanning
* Cloud provider security documentation

---

## 🙌 Acknowledgement

Created for **Cloud Native Ilorin** as part of a community knowledge-sharing initiative.

If this guide helped you, feel free to ⭐ the repository and share it with others.

---

**Secure your secrets. Protect your systems.**
