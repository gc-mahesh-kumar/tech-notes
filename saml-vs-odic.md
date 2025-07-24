# 🔐 SAML vs OIDC – Authentication Protocols Comparison

A concise overview and comparison between **SAML (Security Assertion Markup Language)** and **OIDC (OpenID Connect)** — two widely used authentication protocols in modern and enterprise systems.

---

## 📚 Table of Contents

- [Overview](#overview)
- [Key Differences](#key-differences)
- [Comparison Table](#comparison-table)
- [When to Use What](#when-to-use-what)
- [Summary](#summary)
- [Resources](#resources)

---

## 📖 Overview

Both **SAML** and **OIDC** are authentication protocols used to implement **Single Sign-On (SSO)**. However, they differ in architecture, token format, and target use cases.

- **SAML**: XML-based, older, used in enterprise and legacy applications.
- **OIDC**: JSON-based, built on OAuth 2.0, suited for modern apps and mobile.

---

## ⚖️ Key Differences

| Feature | SAML | OIDC (OpenID Connect) |
|--------|------|------------------------|
| **Protocol Type** | XML-based | JSON/REST-based |
| **Transport** | HTTP POST/Redirect | HTTPS (REST APIs) |
| **Token Format** | SAML Assertion (XML) | ID Token (JWT) |
| **Primary Use** | Enterprise SSO | Web & Mobile App Auth |
| **Standard By** | OASIS | OpenID Foundation |
| **Ease of Use** | Complex (XML, SOAP) | Simple (REST, JSON) |
| **Mobile Friendly** | ❌ No | ✅ Yes |
| **Common Use** | Legacy apps, AD FS | OAuth-based apps, APIs |

---

## 🎯 When to Use What

### ✅ Use **SAML** if:
- You're integrating with legacy or enterprise applications.
- You're working with traditional identity providers (e.g., AD FS, Okta SAML).
- You need SSO support in systems like Salesforce or SAP.

### ✅ Use **OIDC** if:
- You're developing modern web or mobile applications.
- You want to support social login (e.g., Google, Microsoft).
- You need OAuth 2.0 compatibility and access token delegation.

---

## 🧠 Summary

| Aspect | SAML | OIDC |
|--------|------|------|
| Age | Older | Newer |
| Use Case | Enterprise | Modern apps |
| Data Format | XML | JSON |
| Extensibility | Low | High |
| Mobile Support | Poor | Excellent |

---

## 📚 Resources

- [OpenID Connect Specification](https://openid.net/connect/)
- [SAML 2.0 Overview – OASIS](https://docs.oasis-open.org/security/saml/v2.0/)
- [OAuth 2.0 Overview](https://oauth.net/2/)
- [JWT.io – Learn About JSON Web Tokens](https://jwt.io/introduction/)

---

## 👨‍💻 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

