# 01 — P2P Cycle Overview

## The Map

**Upstream (Procurement-owned):**
Need identified → PR raised → PR approved → Sourcing (if new vendor/no contract) → Vendor selected → PO created → PO approved → PO sent to vendor

**Downstream (AP-owned — my strength):**
Goods/Service delivered → GRN (Goods Receipt Note) posted → Invoice received → 3-way match (PO-GRN-Invoice) → Invoice approved → Payment posted → Payment made

## One-liner for interviews

> "Upstream is about deciding what to buy, from whom, and at what price. Downstream is about verifying what was actually delivered matches what was ordered and billed, then paying accurately and on time."

## Why the split matters

Interviewers use this split to test whether a candidate understands P2P as one continuous chain rather than two disconnected functions. Every downstream exception (a hold, a mismatch, a vendor query about payment status) usually traces back to something that happened upstream — a wrong GL code on a PR, a PO price that didn't match the negotiated contract, a GRN that was never posted. Being able to point to *where* in the upstream chain a downstream problem originated is what separates "I process invoices" from "I understand P2P."

## Handoff points to know cold

| From | To | What crosses the handoff |
|---|---|---|
| Requester | Buyer | Approved PR |
| Buyer | Vendor | Issued PO |
| Vendor | Warehouse/Requester | Physical goods or delivered service |
| Warehouse/Requester | AP | GRN posted in system |
| Vendor | AP | Invoice (paper, email, or Ariba Network e-invoice) |
| AP | Vendor | Payment + remittance advice |

Each row is a place where a mismatch or delay can occur — and each is a fair interview question ("what happens if the GRN is never posted?", "what if the PO price doesn't match the invoice?").
