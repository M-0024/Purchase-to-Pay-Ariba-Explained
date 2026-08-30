# 06 — Interview Q&A (In My Own Words)

Format for each: **Question → Answer → Applied example.** Practice saying these out loud, not just reading them.

---

**Q1. Walk me through the P2P cycle end to end.**
A: P2P splits into upstream and downstream. Upstream: a need triggers a PR, the PR is approved, sourcing happens if there's no existing vendor/contract, a PO is created and sent to the vendor. Downstream: goods or services are delivered, a GRN is posted, the invoice arrives, it's 3-way matched against the PO and GRN, approved, and paid.
*Example:* "In my role I sit downstream — I see the outcome of every upstream decision as either a clean invoice or a hold."

---

**Q2. What's the difference between a PR and a PO?**
A: A PR is an internal request — not binding on the vendor, freely editable until approved. A PO is the external, legally binding document the vendor sees and can invoice against.

---

**Q3. What criteria are mandatory to raise a valid PR in Ariba?**
A: Requester and cost center, GL/WBS code, item/service description, quantity and UoM, required date, plant/ship-to, estimated price, and — for non-catalog items — a business justification. Budget availability is often checked at this stage too.

---

**Q4. When does sourcing get triggered instead of a direct PO?**
A: When there's no existing contract or catalog price, when the value crosses a mandatory competitive-bid threshold, or when it's a new spend category or an underperforming vendor needs replacing.

---

**Q5. How do you select a vendor — what factors matter for goods vs services?**
A: Common factors: total cost of ownership, financial stability, compliance, past performance, certifications. For goods: quality consistency, lead time, shelf-life/packaging compliance. For services: SLA commitments, team expertise, scalability.

---

**Q6. What happens if a PR has a wrong GL code — how is it corrected?**
A: It gets rejected by the finance approver and sent back to the requester to correct and resubmit. If it's already converted into a PO, the PR line typically needs to be cancelled and a new, correct PR raised — most systems don't allow editing a PR once it's consumed.

---

**Q7. What's a 3-way match and why does it matter?**
A: It's the check that the PO (what was ordered), the GRN (what was received), and the invoice (what was billed) all agree on quantity and price within tolerance. It's the main control that prevents overpayment or paying for goods never received.

---

**Q8. How does Ariba route PR approvals — what determines the approval chain?**
A: Approval flow rules configured against the PR's value, commodity code, and cost center — low value may auto-approve, higher value escalates through department head, procurement, and finance.

---

**Q9. What's the difference between a catalog and non-catalog requisition?**
A: Catalog requisitions pull pre-negotiated items and pricing, so they're fast and low-error. Non-catalog/free-text requisitions are for items not in any catalog, need manual entry of spec and price, and move slower through approval.

---

**Q10. How do you handle a vendor who's not yet onboarded but needs an urgent PO?**
A: Vendor master setup (tax IDs, banking, compliance docs) has to be completed and the vendor registered before a PO can be legitimately issued and paid — urgency doesn't bypass compliance checks, though some orgs have an expedited onboarding path for genuinely urgent cases.



## Notes to self before the interview
- Don't just define terms — always land on the "why it matters" or a real-world consequence.
- Bridge every upstream answer back to a downstream consequence I've actually seen (hold, mismatch, vendor query) — that's my differentiator over a pure sourcing/buying candidate.
“What’s the difference between catalog and non-catalog buying in Ariba?”
ans:“Catalog buying means employees order from pre-approved supplier catalogs with fixed prices and items — it’s fast and controlled. Non-catalog buying is for items not in catalogs, where users enter details manually, which gives flexibility but requires more approvals and oversight.


