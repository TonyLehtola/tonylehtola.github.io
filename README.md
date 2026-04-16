# Apex Outdoors — Demo Landing Page

> Fictitious outdoor gear & apparel retailer created for the **NiCE Cognigy Agentic AI Demo**.  
> Built as a static GitHub Pages site to serve as a realistic customer-facing backdrop for live demo scenarios.

---

## What This Is

This is a single-file static landing page for **Apex Outdoors** — a fictitious mid-market outdoor gear retailer used as the demo scenario in a NiCE Cognigy Agentic AI presentation. The page provides a realistic web context for the Cognigy webchat widget, grounding the demo in a believable customer experience.

The site is intentionally self-contained — no build tools, no dependencies, no backend. It hosts on GitHub Pages in under two minutes.

---

## Demo Scenario Context

| Field | Detail |
|---|---|
| **Company** | Apex Outdoors |
| **Headquarters** | Boulder, Colorado |
| **Customers** | 2M+ active |
| **Contact Center** | 400 agents, 24/7 support |
| **Platform** | NiCE Cognigy (Agentic AI) |
| **Demo Acts** | Act 1: Digital Chat — Agentic Exchange · Act 2: Voice — Inbound + Escalation |

### Demo Customers

**Sarah M.** — Apex Rewards Summit member  
Email: `sarah.m@apexrewards.com`  
Scenario: Trail Runner X exchange (size 8.5 → size 9), Order `#APX-00481923`

**Marcus T.** — Apex Rewards Explorer member  
Email: `marcus.t@apexrewards.com`  
Scenario: Delayed order inquiry, Order `#APX-00479654`

---

## Quick Start

### Deploy to GitHub Pages

1. Create a new GitHub repository (public)
2. Upload `index.html` to the root of the `main` branch
3. Go to **Settings → Pages**
4. Set source to **Deploy from a branch** → `main` / `(root)`
5. Click **Save** — your site will be live at:

```
https://<your-username>.github.io/<repo-name>/
```

### Add the Cognigy Chat Widget

Open `index.html` and scroll to the very bottom. Find this comment:

```html
<!-- PASTE YOUR COGNIGY SNIPPET HERE -->
```

Replace it with your Cognigy webchat snippet from your endpoint settings. It will look something like this:

```html
<script src="https://webchat.cognigy.ai/v3/webchat.js"
  data-webchat-settings='{
    "baseUrl": "https://endpoint.cognigy.ai/YOUR_ENDPOINT_TOKEN",
    "userId": "",
    "sessionId": "",
    "channel": "webchat3",
    "settings": {
      "colorScheme": "#C8A96E",
      "botAvatarInitials": "AO",
      "title": "Apex Outdoors Support"
    }
  }'>
</script>
```

> **Tip:** Set `colorScheme` to `#C8A96E` to match the Apex Outdoors gold accent color used throughout the page.

---

## File Structure

```
/
└── index.html        # Entire site — all HTML, CSS, and inline SVG
└── README.md         # This file
```

No dependencies. No npm. No build step. Everything is inline.

---

## Page Sections

| Section | Purpose |
|---|---|
| **Hero** | SVG mountain night scene — establishes brand tone |
| **Stats Strip** | 38 locations · 2M+ customers · 4.9★ · 24/7 support |
| **Categories** | Trail Running · Hiking · Camping · Climbing · Backcountry Ski |
| **Featured Product** | Apex Trail Runner X — the product in the Act 1 exchange scenario |
| **Trail Conditions** | 6 real regions — adds content depth and realism |
| **Rewards Program** | Explorer · Summit · Elite tiers — matches knowledge base data |
| **Footer** | Support links, contact info, demo disclaimer |

---

## Demo Flow Reference

### Act 1 — Digital Chat (~8 min)
Customer Sarah M. initiates a chat from this page to exchange trail runners. The Cognigy agent:
1. Authenticates via email lookup
2. Checks exchange eligibility via Knowledge AI (policy document)
3. Initiates return + replacement order simultaneously

**Start the demo:** Open the chat widget on this page and type Sarah's email when prompted.

### Act 2 — Voice (~8 min)
Sarah calls in 10 minutes later to confirm her exchange. The voice agent:
1. Recognizes Sarah from the prior chat session — no re-authentication
2. Confirms replacement shipping details autonomously
3. Escalates a technical waterproofing question to a live agent with full context packet

---

## Customization Notes

- **Brand colors** are defined as CSS variables at the top of the `<style>` block — easy to adjust if needed
- **Customer data** referenced in the demo is hardcoded in the Cognigy flow as Set Context nodes — this page does not make any API calls
- **The demo disclaimer** in the footer (`Fictitious company created for demonstration purposes`) can be removed before screen-sharing if preferred

---

## Disclaimer

Apex Outdoors is a fictitious company created solely for demonstration purposes. All customer names, order numbers, products, and data referenced in this repository and associated Cognigy flows are fabricated. Any resemblance to real companies or individuals is coincidental.

---

*Built for the NiCE Senior Solution Engineer interview presentation — Tony Lehtola, April 2026*
