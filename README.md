# CISS — CIS Secure Transport (Optional Reference Implementation) [![Org](https://img.shields.io/badge/Org-CommonIntents-darkgray.svg)](https://github.com/CommonIntents)

**One possible implementation of CIB, not a mandatory protocol component.**

CISS provides mTLS-based encrypted transport as a reference implementation of the CIB transport binding specification.

CISS is NOT the "skeleton" of the protocol family — transport security is infrastructure, and trust is a multi-dimensional collaboration across the ecosystem (L0 gene-lock hash, Cellrix view hash, Helix-Mind experience verification, Tuck physical isolation).

## Identity Model
The Agent's private key is its local trust anchor. Identity is cryptographically proven at mTLS handshake.

## Protocol Stack
```
CIS (intent syntax)
  ↑
CIB (transport binding)
  ↑
CISS ← You are here (optional mTLS reference implementation)
  ↑
CAP (consensus confirmation)
```

## Read the Spec
- [CISS v0.1.0-draft](spec/CISS.md)
- [中文版](spec/CISS.zh-CN.md)

## Related
| Protocol | Repository |
|:---|:---|
| CIS | [CommonIntents/CIS](https://github.com/CommonIntents/CIS) |
| CAP | [CommonIntents/CAP](https://github.com/CommonIntents/CAP) |
| CIB | [CommonIntents/CIB](https://github.com/CommonIntents/CIB) |

## License
Apache 2.0 — see [LICENSE](LICENSE).
