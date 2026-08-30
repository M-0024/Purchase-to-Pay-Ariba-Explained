# 04 — Purchase Order (PO) Deep Dive

## What is a PO?

A PO is the **external, legally binding** document sent to a vendor once a PR is approved and the vendor/price is confirmed — either from an approved sourcing event, an existing contract/catalog price, or a direct quote for low-value spend.

T code ME21N Create po 
ME22N Change Po 
 ME23N DISPLAY PO

## PO Types

| Type | Description | Typical use |
|---|---|---|
| **Standard PO** | One-time, defined quantity and price | A single, well-specified purchase |
| **Blanket / Framework PO** | Value-limit set upfront, multiple releases drawn down over a period | Recurring services or repeat materials from the same vendor |
| **Contract-referenced PO** | Price pulled automatically from a negotiated contract | Any purchase against an existing Ariba Contract |

## PO Issuance

- Transmitted to the vendor via **Ariba Network (cXML)**, EDI, email, or a vendor portal.
- Vendor acknowledges receipt (and, on Ariba Network, can flip the PO directly into an invoice — reducing invoice errors since it's system-generated from the PO data).

## PO Change / Amendment

- Any change to **quantity, price, or delivery date** after issuance requires a formal **PO change order** — this is not a free edit.
- This is a key control point: auditors specifically check that PO changes are documented and approved, since an uncontrolled PO change is a common fraud/error vector.

## Why this matters downstream

The PO is the anchor document for the **3-way match** (PO–GRN–Invoice). Any inconsistency introduced here — wrong price, wrong quantity, a change order that wasn't properly closed — surfaces later as an invoice hold in AP. This is the direct link between upstream PO discipline and the downstream hold volume you already manage.

## Sample answer structure (for spoken delivery)

1. Define PO and contrast with PR in one line (see file 02 for the full comparison table).
2. Name the three PO types and when each is used.
3. Give one applied example: *"A blanket PO makes sense for a recurring Germany-region freight vendor billed monthly, whereas a standard PO fits a one-time capital equipment purchase."*
