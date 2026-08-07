# 🛡️ Northbridge Kitchen Supply Co. — NIST CSF 2.0 Risk Assessment

**Self-directed GRC portfolio project**

Nobody hands a stranger their real company's cybersecurity environment to practice on — so this project builds one. Northbridge Kitchen Supply Co. is a fictional 42-person B2B distributor of commercial kitchen equipment, given a realistic tech stack and operating model, then run through a full NIST CSF 2.0 risk assessment from scoping to a prioritized remediation roadmap.

> **Northbridge Kitchen Supply Co. does not exist.** This is a fictional, self-directed exercise built to practice and demonstrate the NIST CSF 2.0 methodology end to end. No real organization, data, or finding is described.

## The company

- 42 employees, B2B distributor of commercial kitchen equipment
- Tech stack: Microsoft 365, a WooCommerce/WordPress ordering portal, Salesforce, Stripe, a 3PL warehouse system
- No in-house security team — an Operations Manager covers IT part-time, with an outsourced MSP for helpdesk

That combination is deliberate: it's designed to organically produce the same pattern of gaps a real 40-person distributor would have, not gaps picked to make a good story.

## What's inside

```
northbridge-nist-csf-assessment/
├── README.md
├── LICENSE
├── .gitignore
├── report/
│   └── Northbridge-NIST-CSF-2.0-Executive-Report.pdf
└── workbook/
    └── Northbridge-NIST-CSF-2.0-Risk-Assessment.xlsx
```

### 📄 `report/` — Executive Report
A leadership-facing summary: the maturity heatmap by Function, the top 10 Critical risks, and the 30/90/180-day remediation roadmap.

### 📊 `workbook/` — Companion Workbook
The full methodology, scored at full detail, across four tabs:
- **Read Me** — scope, maturity scale, risk model, and sourcing
- **Function Summary** — the heatmap, computed live via formulas from the register
- **Risk Register** — all 35 scored subcategories: current state, target state, gap, likelihood, impact, risk score, finding, recommendation, owner, and horizon
- **Roadmap** — the same 35 actions grouped into 30/90/180-day horizons

Every subcategory ID and description in the workbook is drawn from the official NIST CSF 2.0 Core. All aggregate numbers are computed live with formulas from the Risk Register tab — change a score there and the rest of the workbook recalculates.

## Methodology

1. **Scope honestly** — NIST CSF 2.0 has 106 subcategories across 6 Functions. Scoring all of them at full depth isn't realistic for a first-pass assessment, so 35 representative subcategories were selected, weighted proportionally to each Function's share of the full framework.
2. **Score current vs. target** — each subcategory scored 0 (Not Implemented) to 3 (Fully Implemented): where Northbridge stands today, and a realistic target for a company its size.
3. **Quantify the risk** — every gap run through a Likelihood × Impact model (1–5 each) for a 1–25 risk score, banded into Low, Medium, High, and Critical.
4. **Turn findings into owned, dated actions** — all 35 gaps map to a recommendation with an owner (Ops Manager, MSP, or Leadership) and a horizon, rolled into a 30/90/180-day roadmap.

## Headline findings

| Metric | Result |
|---|---|
| Average current maturity | 0.23 / 3 |
| Average target maturity | 1.46 / 3 |
| Critical findings | 10 |
| High findings | 9 |
| Highest single risk | `ID.AM-07` — no inventory of where customer PII and payment data actually flow (20/25) |
| Weakest Functions | Govern, Identify |
| Effectively at zero | Detect, Respond, Recover |

## Why this approach

If you're building a portfolio in cyber risk or GRC and don't have access to a real environment yet, this is one way to do it. You don't need someone else's infrastructure to prove you know the process — scoping, scoring, prioritizing, and communicating cybersecurity risk the way you'd want to for a real client or employer.

## License

MIT — see [LICENSE](LICENSE).

---
Fictional exercise, built for portfolio purposes.
