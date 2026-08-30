# 03 — Sourcing & Vendor Selection Deep Dive

## When does sourcing get triggered?

- No existing contract/vendor covers the item or service in the PR.
- Existing contract is expiring, or vendor performance has been poor.
- The PR's value crosses a threshold that mandates competitive bidding under org policy (above a set INR/USD/EUR value, direct award isn't allowed).
- New category of spend — first time buying this type of good or service.

## Sourcing Process Flow

1. **PR flagged for sourcing** — buyer reviews the requisition and confirms no existing catalog/contract covers it.
2. **Market/vendor identification** — buyer builds a longlist from the vendor master, vendor databases, or a new market search.
3. **RFI (Request for Information)** — optional step used to shortlist capable vendors when the field is unclear.
4. **RFP/RFQ issued**:
   - **RFQ (Request for Quotation)** — price-driven, used when the spec is clear.
   - **RFP (Request for Proposal)** — used for complex or service-heavy scope where approach/methodology matters, not just price.
   - Typically managed through the **Ariba Sourcing** module, which runs bid events, sets deadlines, and collects vendor responses in one place.
5. **Bid evaluation** — scored against defined criteria (see below).
6. **Negotiation** — price, payment terms, SLA, delivery timelines.
7. **Vendor award + contract creation** — the winning vendor's terms go into **Ariba Contracts**, which becomes the pricing source for future POs.
8. **PO created** against the contract (or a direct PO for a genuine one-time buy).

## Vendor Selection Criteria

### Common to goods and services
- Price competitiveness / **Total Cost of Ownership** — not just unit price; includes freight, duties, payment terms.
- Financial stability — credit check, D&B rating.
- Compliance — tax registration, GST/VAT validity, sanctions/denied-party screening, ESG/sustainability compliance (increasingly weighted for FMCG companies).
- Past performance / references.
- Capacity to scale and reliability of lead time.
- Quality certifications (ISO, industry-specific).

### For goods (materials, packaging, ingredients)
- Quality consistency and defect rate.
- Delivery lead time and logistics network.
- Minimum order quantity flexibility.
- Packaging/shelf-life compliance — especially relevant for a food & beverage company.

### For services
- Team/resource expertise and credentials.
- SLA commitments — turnaround time, uptime, responsiveness.
- Past project case studies.
- Scalability of resourcing.

## Vendor Onboarding (once selected)

- Vendor master record created in SAP/Ariba — tax IDs, banking details, compliance documents (W-9/W-8 or local equivalent).
- Vendor registered on the **Ariba Network** so they can receive POs and submit invoices electronically (cXML / PO flip).

## Sample answer structure (for spoken delivery)

1. State when sourcing kicks in vs a direct PO.
2. Walk the RFI/RFQ/RFP → evaluation → award sequence in order.
3. Give one applied example distinguishing goods vs services criteria, e.g.: *"For a packaging material vendor I'd weight lead-time reliability and shelf-life compliance heavily; for an IT services vendor I'd weight SLA and resource expertise instead."*

   ## Advanced — Weighted Evaluation & Bid Mechanics

Move from "what factors matter" to "how they're actually weighted and evaluated" — this is the level that signals real understanding rather than a textbook list.

### Weighted scorecard (common in Ariba Sourcing events)

Mature procurement orgs don't just eyeball vendor quotes — they run a weighted scorecard:

| Criterion | Typical weight |
|---|---|
| Price / Total Cost of Ownership | 40–50% |
| Quality / compliance / certifications | 20–25% |
| Delivery reliability / lead time | 15–20% |
| Service/support/SLA | 10–15% |

Being able to say *"it's not just lowest price — it's a weighted scorecard where price is heavy but not sole"* signals real understanding.

### Bid types worth distinguishing

- **Sealed bid** — all vendors submit blind, opened together; prevents undercutting mid-process.
- **Reverse auction** — vendors see (anonymized) competing bids live and can revise downward in real time; used for highly commoditized, price-sensitive spend (e.g., raw packaging materials), not for complex services.
- **Multi-round RFP** — shortlist after round 1, deeper technical/commercial negotiation in round 2; used for services or strategic categories.

### Compliance gates (pass/fail, before scoring even starts)

- Sanctions/denied-party list screening (OFAC, EU consolidated list) — an automatic disqualifier, not a scored criterion.
- Conflict-of-interest declaration.
- Minimum insurance/certification thresholds (e.g., ISO 22000 for a food-adjacent vendor at a company like PepsiCo) — pass/fail gate, not weighted.

**Follow-up they might ask:** *"How do you handle a vendor who scores best commercially but fails a compliance gate?"*
→ Compliance gates are pass/fail and sit *before* the scorecard — a vendor that fails one is disqualified regardless of price, because it's a legal/regulatory risk, not a commercial trade-off.

