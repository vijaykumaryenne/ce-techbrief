# CE TechBrief
### AI-Powered Customer Technical Brief Generator
**Oracle Cloud Engineering · JAPAC AI Challenge · FY27**

---

## What it does

CE TechBrief generates a structured, customer-specific technical brief in under 5 minutes. A Cloud Engineer enters the company name, industry, opportunity type, Oracle products in scope, and any known context. The tool returns a complete pre-meeting brief covering:

- **Assumed current stack** — cloud/infra environment, database tier, middleware, legacy constraints
- **Likely pain points** — 3 industry-calibrated pain points specific to the customer's situation
- **Oracle solution angles** — per-product value angle tailored to this customer, not generic positioning
- **Discovery questions** — 5 sharp, open-ended questions built for the specific meeting type
- **Watch-outs** — likely objections and sensitivities to anticipate
- **Competitor alert** — most likely competitor presence and the key differentiator to lead with

---

## The problem it solves

Cloud Engineers spend 30–60 minutes manually researching accounts before every customer meeting. The output is inconsistent across the team, often thin under time pressure, and rarely reflects the full picture a CE needs to engage credibly at a technical level.

Across ~200 CEs in JAPAC, that is thousands of hours per year spent on commodity prep work instead of customer impact. CE TechBrief eliminates the preparation gap without replacing CE judgment.

---

## Live demo

👉 **[Launch CE TechBrief](https://vijaykumaryenne.github.io/ce-techbrief/ce_brief_generator.html)**

---

## How to use it

1. Open the link above in any modern browser
2. Fill in the engagement context on the left panel:
   - Company name
   - Industry
   - Opportunity type (New Logo / Expansion / Renewal / Migration)
   - Oracle products in scope
   - Any known context (paste news, stack info, pain points)
   - Meeting type
3. Click **Generate Technical Brief**
4. Review the brief on the right panel
5. Use **Copy to Clipboard** to paste into your notes or CRM

---

## How it works

The tool sends the engagement context to the Claude API (Anthropic) with a structured prompt that instructs the model to return a JSON brief calibrated to the customer's industry, opportunity type, and meeting context. The response is parsed and rendered into the brief UI client-side.

```
CE inputs context
        ↓
Structured prompt sent to Claude API
        ↓
JSON brief returned (stack / pain points / pitch / questions / watch-outs)
        ↓
Brief rendered in UI — ready in under 5 minutes
```

### The core prompt

```
You are a seasoned Oracle Cloud Engineer preparing a pre-meeting
technical brief for an Oracle sales engagement.
Return ONLY a valid JSON object. No markdown, no backticks,
no explanation before or after.

Engagement details:
Company: [company name]
Industry: [industry]
Opportunity type: [New Logo / Expansion / Renewal / Migration]
Oracle products in scope: [e.g. OCI, Gen AI, AI Autonomous DB]
Meeting type: [Initial Discovery / Technical Deep Dive / PoC Kickoff ...]
Known context: [any known facts about the customer]
```

---

## Estimated impact

| Metric | Conservative | Likely | Upside |
|--------|-------------|--------|--------|
| Prep time saved per engagement | 20 min | 40 min | 60 min |
| CE engagements briefed per week (JAPAC) | 200 | 350 | 500 |
| Hours saved per week | 67 | 233 | 500 |
| FTE equivalent per year | 1.7 | 5.8 | 12.5 |

---

## What's next

| Phase | Description |
|-------|-------------|
| **Now** | Standalone web tool. Works today with no infrastructure required. |
| **Next** | CRM integration — pull Oracle Sales / Salesforce opportunity data automatically, zero manual input. |
| **Later** | Post-meeting debrief mode — paste call notes, get an updated brief and recommended next actions. |

---

## Files

| File | Description |
|------|-------------|
| `ce_brief_generator.html` | The working tool — open in any browser |
| `ce_techbrief_demo.html` | Animated demo walkthrough (Westpac scenario) |
| `CE_TechBrief_JAPAC_AI_Challenge.docx` | Submission one-pager |

---

## Submission details

- **Category:** Team Productivity — The Force Multiplier
- **Effort:** Team
- **Challenge:** JAPAC AI Challenge, FY27 Sales Kickoff
- **Submitted by:** Vijay Kumar Yenne, Director of Cloud Architects, Oracle JAPAC

---

*Built with Claude (Anthropic) · Oracle Cloud Engineering · June 2026*
