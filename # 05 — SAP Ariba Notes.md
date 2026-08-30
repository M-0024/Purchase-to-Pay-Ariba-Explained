# 05 — SAP Ariba Notes

## Core Modules and Where They Sit in P2P

| Module | Role in P2P |
|---|---|
| **Ariba Buying** | Where requisitions (PRs) are raised — catalog and non-catalog — and where POs are generated once a PR is approved |
| **Ariba Sourcing** | Runs RFI/RFQ/RFP bid events, manages vendor responses, scoring, and award decisions |
| **Ariba Contracts** | Stores negotiated terms/pricing from awarded sourcing events; feeds pricing into future contract-referenced POs |
| **Ariba Network** | The vendor-facing layer — vendors receive POs, acknowledge them, and submit invoices electronically (cXML / PO flip) |

## How a PR/PO Actually Flows Through Ariba

1. Requester raises a requisition in **Ariba Buying** (catalog or non-catalog).
2. Requisition routes through configured **approval flow rules** (based on amount, commodity code, cost center).
3. If no contract/catalog price exists and the value crosses a sourcing threshold, the buyer kicks off an event in **Ariba Sourcing**.
4. Once a vendor is awarded, terms are captured in **Ariba Contracts**.
5. Buyer converts the approved requisition into a PO in **Ariba Buying**, referencing the contract price if one exists.
5. PO transmits to the vendor via **Ariba Network**.
6. Vendor acknowledges and can "flip" the PO into an invoice directly on the Network — this is what reduces invoice-line errors compared to manually keyed invoices.

## Catalog vs Non-Catalog Requisitions

- **Catalog (punch-out/hosted):** pre-negotiated items, pricing already loaded, minimal manual entry, fastest approval path.
- **Non-catalog (free-text):** used for anything not in a catalog — requires the requester to manually enter description, spec, estimated price, and often a business justification. Slower and more error-prone, which is why buyers push spend toward catalogs where possible.

## Why Ariba Matters for the AP/Downstream Side

- E-invoicing via PO flip on the Ariba Network is a major reason invoice-to-PO mismatches are lower for Network-registered vendors versus vendors still sending PDF/paper invoices.
- Understanding which vendors are Network-enabled vs not explains a lot of the variance in hold rates and processing time across a vendor base — a useful point to raise if asked about improving AP efficiency.

## Sample answer structure (for spoken delivery)

1. Name the four modules and their one-line roles.
2. Walk the PR → Sourcing → Contract → PO → Network flow in order.
3. Give one applied example tying it back to AP: *"Vendors onboarded on the Ariba Network and using PO flip generate cleaner invoices with far fewer 3-way match holds than vendors still emailing PDF invoices — which directly affects the hold volume I manage."*
