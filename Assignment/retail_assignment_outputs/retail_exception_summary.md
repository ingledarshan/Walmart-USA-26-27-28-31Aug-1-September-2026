# Retail Shelf Availability Exception Summary

| Case | Action | Confidence | Policy references | Risk flags |
|---|---|---:|---|---|
| EX-101 | REPLENISH_FROM_BACKROOM | 0.95 | POL-INV-01 | — |
| EX-102 | WAIT_FOR_INBOUND | 0.91 | POL-INB-02 | — |
| EX-103 | TRANSFER_FROM_NEARBY_STORE | 0.88 | POL-TRN-03 | — |
| EX-104 | REPLENISH_FROM_BACKROOM | 0.72 | POL-INV-01, POL-SAF-05 | INVENTORY_CACHE_USED, VERIFY_BEFORE_ACTION |

## Limitation
The local retriever and in-memory tools are suitable for a bounded lab, not for production freshness, access control or scale.

## Production-hardening recommendation
Expose governed tools through authenticated REST/MCP services, add tracing and service-level objectives, version policy chunks, and evaluate routing against labelled retail exceptions before enabling operational actions.