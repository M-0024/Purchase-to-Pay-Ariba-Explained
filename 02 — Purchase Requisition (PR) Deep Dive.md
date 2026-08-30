# 02 — Purchase Requisition (PR) Deep Dive

## What is a PR?

An internal document raised by a requester (business user/department) to formally request procurement to buy goods or services. It is **not** a legal commitment to the vendor — it's an internal approval trigger. The PO is what commits the company externally.

## Who raises a PR, and what triggers it

- A department (Marketing, Plant Ops, IT) identifies a need — stock running low, new project, contract renewal, one-time purchase.
- Triggers can be:
  - **Manual** — a user logs into Ariba/SAP and raises it directly.
  - **System-generated** — an MRP run in SAP triggers an auto-PR when stock falls below the reorder point.
  - **Catalog-based** — a user picks an item from a punch-out or hosted catalog in Ariba, and the PR auto-generates from that selection.
- In **Ariba Buying**, the requester raises the requisition via:
  - a **catalog** request (punch-out/hosted catalog, pre-negotiated items — fastest path, least manual detail needed), or
  - a **non-catalog / free-text** request (for items not in any catalog — requires more manual detail: description, specs, estimated price, vendor if known).
  -Create purchase requisition  T code ME51N
  - 
  - <img width="651" height="313" alt="image" src="https://github.com/user-attachments/assets/6a9aa203-b778-46f5-b2b1-355b5b5e7437" />
  <img width="241" height="181" alt="image" src="https://github.com/user-attachments/assets/9b31ed5f-3a62-4dfb-8fa4-0b94bb9003a9" />
  <img width="395" height="258" alt="image" src="https://github.com/user-attachments/assets/43147507-f065-4b7d-978f-4c7e0dea9f1a" />
  
<img width="254" height="135" alt="image" src="https://github.com/user-attachments/assets/49b24bfa-44e7-433b-8768-b54255e3f275" />
<img width="632" height="271" alt="image" src="https://github.com/user-attachments/assets/4ea10f85-631b-4da6-83b6-547aa917e172" />



  youtube link: https://www.youtube.com/watch?v=6P9w40x4Ptg
  https://www.youtube.com/watch?v=mrMUKCfRF5I


## Required fields / criteria to raise a valid PR

- Requester name, cost center, department
- GL account or WBS element (for cost allocation)
- Material/service description, or material code if it exists in master data
- Quantity and unit of measure
- Required delivery date
- Plant/location/ship-to address
- Estimated price (from historical PO, quote, or catalog price)
- Budget availability (some orgs enforce a budget check before the PR can even be submitted)
- Justification/business reason — especially for non-catalog or high-value items
- Preferred vendor, if any (doesn't bypass mandatory sourcing thresholds)

## PR Approval Workflow

- Usually tiered by **value threshold** — e.g., low-value auto-approved or single-level sign-off; higher bands escalate through department head → procurement → finance.
- Ariba routes this automatically through **approval flow rules** configured against amount, commodity code, and cost center.
- Budget check commonly happens at this stage — a PR can be blocked if the cost center is already over budget.

## PR Correction — Common Errors and Fixes

| Error | Effect | Fix |
|---|---|---|
| Wrong GL/cost center | Rejected by finance approver, sent back to requester | Requester edits and resubmits |
| Wrong plant/ship-to | Causes GRN mismatch later in the cycle | Correct before PO conversion |
| Missing/incorrect commodity code | Routes to wrong buyer or wrong approval chain | Requester or buyer corrects the code |
| Price far off market/catalog | Flagged by buyer for review | Buyer queries requester, updates estimate |

**Important nuance:** most systems don't allow editing a PR once it has been consumed by a PO. If a correction is needed post-conversion, the typical path is: cancel/withdraw the PR line → raise a new PR with correct data.

## PR vs PO — the distinction interviewers test most

| | PR | PO |
|---|---|---|
| Nature | Internal request | External legal commitment |
| Visible to vendor | No | Yes |
| Can be freely edited | Yes, until approved/converted | Limited — needs a formal PO change process |
| Owner | Requester/business | Buyer/Procurement |

## Sample answer structure (for spoken delivery)

1. Define it in one sentence.
2. Walk the trigger → fields → approval → conversion sequence in order.
3. Give one applied example: *"For example, in a Germany plant scenario, a requester raising a PR for a packaging material below reorder point would trigger an MRP auto-PR, routed to the plant buyer, checked against budget, and converted to a PO once a valid vendor/contract price exists."*
