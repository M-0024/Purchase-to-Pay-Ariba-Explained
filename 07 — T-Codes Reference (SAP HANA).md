# 07 — T-Codes Reference (SAP HANA) & Why Ariba Has None

SAP S/4HANA still runs on the classic MM transaction codes under the hood, even though the default UI is now Fiori apps. **Ariba is a pure cloud SaaS system with no transaction-code concept at all** — that distinction is worth stating confidently if asked, since it shows you understand the two platforms aren't architecturally the same thing.

## Purchase Requisition (PR)

| T-Code | Function |
|---|---|
| ME51N | Create PR |
| ME52N | Change PR |
| ME53N | Display PR |
| ME54N | Release (approve) PR |
| ME5A | List display of PRs |
| ME56 | Assign source of supply to PR |
| ME57 | Assign and process PRs |

## Sourcing / Vendor Comparison

| T-Code | Function |
|---|---|
| ME41 | Create RFQ |
| ME42 | Change RFQ |
| ME43 | Display RFQ |
| ME47 | Maintain vendor quotation |
| ME49 | Price comparison of quotations |
| ME01 | Maintain source list |
| ME03 | Display source list |
| ME11 | Create purchasing info record |
| ME12 / ME13 | Change / display info record |
| MEQ1 | Maintain quota arrangement |

## Vendor Master

| T-Code | Function |
|---|---|
| XK01 / XK02 / XK03 | Create / change / display vendor centrally (purchasing + accounting) |
| MK01 / MK02 / MK03 | Vendor master at purchasing org level only |
| FK01 / FK02 / FK03 | Vendor master at company code (accounting) level only |

## Contracts / Scheduling Agreements

| T-Code | Function |
|---|---|
| ME31K / ME32K / ME33K | Create / change / display contract |
| ME31L | Create scheduling agreement |
| ME38 | Maintain delivery schedule |

## Purchase Order (PO)

| T-Code | Function |
|---|---|
| ME21N | Create PO |
| ME22N | Change PO |
| ME23N | Display PO |
| ME28 | Release (approve) PO |
| ME2L / ME2M | List POs by vendor / by material |
| ME9F | Output message (send/print/e-transmit PO) |

## Goods Receipt (downstream handoff)

| T-Code | Function |
|---|---|
| MIGO | Post goods receipt against PO (the main one) |
| ML81N | Create/maintain Service Entry Sheet — service PO equivalent of GRN |

## Invoice Verification (MM side, before AP posting)

| T-Code | Function |
|---|---|
| MIRO | Enter incoming invoice / 3-way match |
| MIR7 | Park invoice |
| MRBR | Release blocked invoices (holds) |
| MIR4 | Display invoice document |
| MR8M | Cancel invoice document |

## S/4HANA Note

Most of these T-codes still work as-is via SAP GUI, but S/4HANA's default UI is **Fiori apps** — e.g., "Manage Purchase Requisitions," "Create Purchase Order – Advanced," "Manage Service Entry Sheets." Safe interview line: *"The underlying transaction is still ME51N/ME21N-equivalent, exposed through a Fiori tile."*

## Ariba Note — No T-Codes

Ariba's navigation is menu/workspace-based, not code-based. Instead of a T-code, reference it by **object type**:
- Requisition = PR equivalent
- Sourcing Project = RFQ/RFP equivalent
- Contract Workspace = contract equivalent
- Purchase Order = PO (same term, different platform)

If asked for the "PO T-code in Ariba," the correct answer is that Ariba has no T-codes — that's a SAP GUI-specific concept — and naming that distinction clearly is itself a good signal of real platform knowledge rather than memorized code lists.
