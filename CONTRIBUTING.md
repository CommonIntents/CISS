# Contributing to CISS

CISS (Secure Intent & Control Protocol) is the skeleton of the protocol family.

## Specification Files

- English: [spec/CISS.md](spec/CISS.md)
- Chinese: [spec/CISS.zh-CN.md](spec/CISS.zh-CN.md)

## How to Propose Changes

1. Read the [organization-level contribution guide](https://github.com/CommonIntents/.github/blob/main/CONTRIBUTING.md)
2. Open an Issue describing the problem or improvement you've identified
3. CISS is a transport security implementation; proposals should remain within its scope
4. Update both the English and Chinese versions in your PR

## Scope Constraint

CISS is responsible for transport security only. It does not define intent semantics (CIS),
authorization logic (CAP), or format negotiation (CIB). Proposals crossing these boundaries
will be redirected to the appropriate protocol.
