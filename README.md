SME Support Chatbot

Deterministic Support MVP — Python + Flask (2025)

Executive Summary

Transferable non-SaaS digital asset: deterministic (rule-based) customer support chatbot built in Python + Flask, delivered with a local web demo, portable execution, and a content packs system.

Designed to reduce repetitive support tickets with zero operating cost (no paid AI, no external APIs), offering a clean, auditable, and enterprise-ready structure.

This asset is suitable for:

Direct resale (asset sale)

Integration into larger platforms

Conversion into a SaaS by the buyer (optional, not included)

Delivered as a local/demo-ready asset.
Not a hosted service.

What It Solves (Real Business Value)

Eliminates repetitive customer questions (hours, contact, policies, FAQs)

Reduces support workload for SMEs and small teams

Guarantees consistent, controlled answers (no hallucinations)

Fast adaptation to new clients, sectors, or languages via content packs

Key Technical Highlights (Value Drivers)

Python backend (high transferability, large buyer pool)

Deterministic engine (safe, predictable, audit-friendly)

Zero dependency on AI / LLMs → no running costs

Portable execution (no global setup required)

Clean separation between logic, content, UI, and delivery

Commercial-ready delivery (clean tree, no secrets, no venv)

What’s Included (What Exists Today)
Core

Deterministic response engine (keyword / phrase matching)

Safe fallback response when no match is found

External FAQ dictionaries (JSON-based)

Conversation logging (logs/conversations.log)

Web Demo

Flask web interface

Clean, neutral UI

No hard-coded paths or fragile routing

Content System

Live dictionary

data/faqs.json


Templates & packs

data/examples/faqs_TEMPLATE.json
data/packs/en/faqs_en.json
data/packs/en/faqs_en_hotel.json


Language or sector switching without touching code.

Delivery & Ops

Portable run.ps1 (creates venv only if needed)

Dependency check before install

verify.ps1 for structure + HTTP health check

.env.example (no secrets shipped)

Clean .gitignore

Content Packs (How Customization Works)

The chatbot logic never changes.
Only the content does.

Active dictionary

data/faqs.json


Switch language / sector

# English (generic)
Copy-Item .\data\packs\en\faqs_en.json .\data\faqs.json -Force

# English (hotel sector)
Copy-Item .\data\packs\en\faqs_en_hotel.json .\data\faqs.json -Force


UTF-8 JSON

No code changes

Immediate effect

How to Run (Windows / PowerShell)

From the project root or from dist/:

.\run.ps1


Then open:

http://127.0.0.1:5000


Stop server:

CTRL + C


Optional CLI mode:

python main.py

Project Structure (Final, Clean State)
chatbot_pyme/
├─ admin/
│  ├─ manager.py
│  └─ legacy/
│     └─ demo_legacy.py
├─ data/
│  ├─ faqs.json
│  ├─ examples/
│  │  └─ faqs_TEMPLATE.json
│  └─ packs/
│     ├─ README.txt
│     └─ en/
│        ├─ faqs_en.json
│        └─ faqs_en_hotel.json
├─ logs/
│  └─ conversations.log
├─ src/
│  └─ bot.py
├─ templates/
│  └─ demo.html
├─ interface.py
├─ main.py
├─ requirements.txt
├─ run.ps1
├─ verify.ps1
├─ DELIVERY_CHECKLIST.md
├─ PROCEDURE_TRACKING.md
├─ LICENSE.md
├─ README.md
├─ .env.example
└─ .gitignore

Delivery & Control Files
DELIVERY_CHECKLIST.md

Defines exactly:

What the buyer receives

What is verified

What is not included

Delivery format

PROCEDURE_TRACKING.md

Internal procedure to:

Track completed tasks

Avoid duplicated work

Ensure consistent, auditable delivery

Notes

venv/ is not part of the asset

.env with real keys is never delivered

Tree validated by automated verification

What’s NOT Included (Explicit Limits)

Hosting

User accounts

Payments

Web admin panel

Generative AI / LLMs

Advanced NLP

These exclusions are intentional to keep the asset:

Lean

Transferable

Cost-free

Low-risk for buyers

License

See LICENSE.md.

Summary:

Buyer gets usage, modification, integration, and resale rights

No automatic exclusivity unless contractually agreed

Author may reuse the code independently

Asset Positioning (Market Reality)

Category: Non-SaaS Digital Asset / Support Automation Tool

Technology: Python + Flask

Operating cost: ~0 €

Target buyers:

Agencies

SaaS founders

SMEs

Automation consultants 
---

## Available Content Packs (Ready to Use)

The following sector-specific content packs are included and ready to activate
by copying them over the live dictionary (data/faqs.json).

### Clinic / Healthcare
- English: data/packs/en/faqs_en_clinic.json
- Spanish: data/packs/es/faqs_es_clinic.json

These packs are fully editable UTF-8 JSON files and require no code changes.


---

## Verification & Proof of Functionality

The asset includes an automated verification script (erify.ps1).

Latest execution result:
- STRUCTURE OK
- HTTP GET OK (200)

See TEST_RESULTS.md for recorded verification output.


---

## Delivery State (Current)

- Project structure verified (verify.ps1)
- Web demo responding HTTP 200
- Content packs included and tested
- No secrets included (.env.example only)
- Ready for transfer as a non-SaaS digital asset

This repository represents the final, clean delivery state of the asset.

