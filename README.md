# CISS — Secure Intent & Control Protocol

[![Org](https://img.shields.io/badge/Org-CommonIntents-darkgray.svg)](https://github.com/CommonIntents)

**Structural security, proven at the first millisecond.**

CISS is the transport security implementation based on mTLS. It establishes an end-to-end encrypted channel between Agent and tool, and completes cryptographic identity proof before the first byte of application data is exchanged.

CISS is the **skeleton** of the CIS/CAP protocol family.

## Identity Model

The Agent's private key is its sole trust anchor. Identity is cryptographically proven at mTLS handshake — no centralized tokens required.

```
Agent                          Server
  ├─── TLS ClientHello ────────►
  │◄── CertificateRequest ──────┤
  ├─── Client Certificate ─────►
  ├─── CertificateVerify ──────►  (signed with private key)
  │◄── Handshake Complete ──────┤  ← identity proven
  ├─── Encrypted CIS/CAP Data ──►
```

## Protocol Stack

```
CIS  (intent semantics)
 ↑
CIB  (transport binding)
 ↑
CISS ← You are here
 ↑
CAP  (capability auth & HITL)
```

## Read the Spec

- [CISS v0.1.0-draft](spec/CISS.md)
- [中文版](spec/CISS.zh-CN.md)

## Related

| Protocol | Repository |
|----------|------------|
| CIS | [CommonIntents/CIS](https://github.com/CommonIntents/CIS) |
| CAP | [CommonIntents/CAP](https://github.com/CommonIntents/CAP) |
| CIB | [CommonIntents/CIB](https://github.com/CommonIntents/CIB) |

## License

Apache 2.0 — see [LICENSE](LICENSE).
