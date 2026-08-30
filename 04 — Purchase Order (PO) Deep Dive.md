# 04 — Purchase Order (PO) Deep Dive

## What is a PO?

A PO is the **external, legally binding** document sent to a vendor once a PR is approved and the vendor/price is confirmed — either from an approved sourcing event, an existing contract/catalog price, or a direct quote for low-value spend.

T code ME21N Create po /
ME22N Change Po /
 ME23N DISPLAY PO/
 https://www.youtube.com/watch?v=vK8lYA0pf6g

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
   ## Advanced — PO Type Nuances

Beyond Standard / Blanket / Contract-referenced, these are the nuances that come up in real Ariba/SAP environments and in follow-up questions:

- **Standard PO** — single delivery expected (or a few scheduled lines), fixed price and quantity known upfront.
- **Blanket/Framework PO** (a.k.a. Contract PO in some SAP configs) — a value or quantity ceiling set for a period (e.g., "€50,000 over 12 months"), with individual **releases** drawn down against it as needed. Common for indirect services (cleaning, temp staffing, freight) where exact monthly quantity isn't known upfront.
- **Contract-Referenced PO** — technically a Standard PO that *pulls its price and terms* from an existing outline agreement rather than the buyer keying price manually. Reduces price-entry error and is why contract compliance % is a KPI procurement teams track.
- **Service PO** — distinct because it uses **service entry sheets (SES)** instead of a GRN. The "receipt" of a service is the requester approving the SES, which then feeds the 3-way match in place of a goods receipt. Common trip-up question: *"how does 3-way match work for services if there's no physical goods receipt?"* → SES replaces GRN in the match.
- **Consignment PO** — vendor stock sits on your premises but isn't paid for until consumed/withdrawn; payment triggers off consumption, not delivery.
- **Subcontracting PO** — you send raw materials to a vendor who returns a finished/semi-finished good; the PO tracks both the outbound materials and the returned value-added product.

**Follow-up they might ask:** *"Why would a blanket PO be risky if not managed properly?"*
→ Releases can be drawn down without fresh scrutiny each time — if nobody's tracking cumulative spend against the ceiling, you can breach the authorized value before anyone notices. That's why blanket POs usually have automated alerts at 80–90% consumption.

