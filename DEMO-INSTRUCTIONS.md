# GuitarSales Demo Instructions

Classification: Public

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this repository.

## Quick explanation

This demo shows how a seller or business leader at **Northstar Acoustic Works**, a fictional Microsoft Fake Company, can chain Microsoft 365 Copilot Agents to move from regional sales data to an executive brief and meeting presentation, then create focused agents for shop safety and product-build planning.

Use these materials in a demo-safe Microsoft 365 tenant. All data, documents, personas, and metrics are fictional.

## Demo objective and target audience

- **Objective:** Demonstrate agent chaining and agent creation using only the requested tools: Analyst agent, Word agent, PowerPoint agent, SharePoint agent creation, and chat agent creation.
- **Audience:** M365 Copilot customers, business decision makers, sales operations leaders, manufacturing leaders, and MTT private-delivery attendees.
- **Primary persona:** Morgan Ellis, fictional VP of Sales and Operations at Northstar Acoustic Works.

## Prerequisites

- Microsoft 365 Copilot with Analyst agent, Word agent, and PowerPoint agent available.
- A demo-safe SharePoint document library for grounding files.
- A demo-safe Teams group chat for sharing the SharePoint SOP agent.
- Files from `artifacts/`, `sample-data/`, and `setup/` uploaded to the demo location.

## Workflow overview

| Order | Tool | Input artifacts | Output |
|---|---|---|---|
| 1 | Analyst agent | Regional CSV/XLSX files and dashboard template | A new regional sales analysis workbook |
| 2 | Word agent | New workbook, sales brief template, source URLs | Executive sales brief |
| 3 | PowerPoint agent | Sales brief and meeting deck starter | Meeting presentation |
| 4 | SharePoint agent | Shop accident SOP | SOP Q&A agent shared to Teams group chat |
| 5 | Chat agent | Build guidelines and wood supplies workbook | Build-planning and wood-availability assistant |

## Step-by-step demo script

### 1. Analyst agent creates a workbook from the template (6 minutes)

Open the Analyst agent with the dashboard template and regional sales files.

#### Prompt box: Analyst agent

```text
Create a new workbook from the Northstar dashboard template. Import all regional sales CSV files, refresh the dashboard, identify the top three regional opportunities, and save the result as Northstar_August_Regional_Sales_Analysis.xlsx. Include a short summary sheet with revenue, margin, unit volume, accessory attach opportunity, and recommended follow-up by region.
```

Expected outcome: a refreshed workbook that keeps the dashboard structure while using the regional sales data as inputs.

### 2. Word agent creates the sales brief (6 minutes)

Open Word agent with the generated workbook and `Northstar_Sales_Brief_Template.docx`.

#### Prompt box: Word agent

```text
Using the new analysis workbook and the sales brief template, draft a two-page executive sales brief for Morgan Ellis. Include the strongest regional revenue story, gross margin risks, accessory attach-rate opportunities, and a market-news paragraph based on these public source URLs: https://www.martinguitar.com/, https://www.namm.org/news, and https://musictrades.com/. Keep the company, people, and metrics fictional and mark the brief Classification: Public.
```

Expected outcome: a concise sales brief that cites public source URLs and makes recommendations from synthetic sales data.

### 3. PowerPoint agent creates the meeting deck (5 minutes)

Open PowerPoint agent with the sales brief and starter deck.

#### Prompt box: PowerPoint agent

```text
Create a five-slide leadership meeting deck from the sales brief and the starter deck. Include: 1) objective and workflow, 2) regional revenue story, 3) category mix and accessory attach opportunity, 4) supply and wood-availability risk, and 5) leadership decisions needed. Use executive language and keep all content Classification: Public.
```

Expected outcome: a meeting-ready presentation for the leadership discussion.

### 4. Build a SharePoint SOP agent and share to Teams (7 minutes)

Use `Northstar_Shop_Accident_Response_SOP.docx` as the grounding file.

#### Agent instruction box: SharePoint SOP agent

```text
You are the Northstar Shop Safety Assistant. Answer only from the Shop Accident Response SOP. Cite the relevant SOP section in every answer. Do not provide medical diagnosis. For urgent or ambiguous incidents, direct the user to emergency services or the site safety lead. Keep the answer concise and action-oriented.
```

#### Prompt box: SharePoint SOP agent test

```text
A supervisor reports a minor cut at the fret station and production is paused. What should they do first, what must they document, and when can work restart?
```

Expected outcome: an SOP-grounded answer with section citations and a safe escalation boundary. Share the agent to the Teams group chat after validating the behavior.

### 5. Build a chat agent for product-build planning (7 minutes)

Use `Northstar_Product_Build_Guidelines.docx` and `Northstar_Wood_Supplies_Availability.xlsx` as grounding files.

#### Agent instruction box: Chat build-planning agent

```text
You are the Northstar Build Planning Assistant. Use the product build guidelines and wood supplies workbook to recommend wood options, substitutions, and availability caveats. Cite material IDs when making availability recommendations. Ask for product family, run size, or tonal goal if the request is incomplete. Keep all answers grounded in the Public demo files.
```

#### Prompt box: Chat build-planning agent test

```text
We need to plan 120 Aurora Dreadnought units for a dealer campaign. Which soundboard and back-and-side materials should we use if we want low supply risk and a balanced voice?
```

Expected outcome: a grounded answer that cites wood inventory material IDs and explains substitutions or caveats.

## Suggested talk track

“The value is not one clever prompt. The value is a connected workstream. Analyst agent turns raw regional data into a workbook, Word agent turns that analysis into an executive brief with market context, PowerPoint agent prepares the meeting, and two scoped agents keep operational knowledge available where people work.”

## Validation points

- The generated workbook uses the template rather than starting from a blank workbook.
- The sales brief cites public source URLs but does not claim real customer data.
- The PowerPoint deck reflects the brief and analysis.
- The SharePoint SOP agent answers only from the SOP.
- The chat agent cites material IDs from the wood workbook.

## Troubleshooting

| Issue | Suggested fix |
|---|---|
| Analyst agent does not import all regional files | Upload `sample-data/all_regions_sales.csv` as a fallback single source. |
| Word brief uses real company names | Re-run with the instruction to keep all company and metric content fictional. |
| PowerPoint deck is too generic | Provide the sales brief and starter deck together, then ask for leadership decisions and regional priorities. |
| SOP agent answers beyond the SOP | Tighten instructions to answer only from grounded files and cite sections. |
| Chat agent does not cite material IDs | Ask it to cite `MaterialID` from the workbook in every material recommendation. |

## Supporting files

- [sample-data/northeast_regional_sales.csv](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/northeast_regional_sales.csv)
- [sample-data/southeast_regional_sales.csv](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/southeast_regional_sales.csv)
- [sample-data/midwest_regional_sales.csv](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/midwest_regional_sales.csv)
- [sample-data/southwest_regional_sales.csv](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/southwest_regional_sales.csv)
- [sample-data/west_regional_sales.csv](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/west_regional_sales.csv)
- [sample-data/all_regions_sales.csv](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/all_regions_sales.csv)
- [sample-data/northeast_regional_sales.xlsx](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/northeast_regional_sales.xlsx)
- [sample-data/southeast_regional_sales.xlsx](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/southeast_regional_sales.xlsx)
- [sample-data/midwest_regional_sales.xlsx](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/midwest_regional_sales.xlsx)
- [sample-data/southwest_regional_sales.xlsx](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/southwest_regional_sales.xlsx)
- [sample-data/west_regional_sales.xlsx](https://github.com/AndrewConniff/GuitarSales/blob/main/sample-data/west_regional_sales.xlsx)
- [artifacts/Northstar_Acoustic_Works_Sales_Dashboard_Template.xlsx](https://github.com/AndrewConniff/GuitarSales/blob/main/artifacts/Northstar_Acoustic_Works_Sales_Dashboard_Template.xlsx)
- [artifacts/Northstar_Wood_Supplies_Availability.xlsx](https://github.com/AndrewConniff/GuitarSales/blob/main/artifacts/Northstar_Wood_Supplies_Availability.xlsx)
- [artifacts/Northstar_Sales_Brief_Template.docx](https://github.com/AndrewConniff/GuitarSales/blob/main/artifacts/Northstar_Sales_Brief_Template.docx)
- [artifacts/Northstar_Shop_Accident_Response_SOP.docx](https://github.com/AndrewConniff/GuitarSales/blob/main/artifacts/Northstar_Shop_Accident_Response_SOP.docx)
- [artifacts/Northstar_Product_Build_Guidelines.docx](https://github.com/AndrewConniff/GuitarSales/blob/main/artifacts/Northstar_Product_Build_Guidelines.docx)
- [artifacts/Northstar_GuitarSales_Meeting_Deck.pptx](https://github.com/AndrewConniff/GuitarSales/blob/main/artifacts/Northstar_GuitarSales_Meeting_Deck.pptx)
- [setup/sharepoint_safety_agent_config.json](https://github.com/AndrewConniff/GuitarSales/blob/main/setup/sharepoint_safety_agent_config.json)
- [setup/chat_build_planning_agent_config.json](https://github.com/AndrewConniff/GuitarSales/blob/main/setup/chat_build_planning_agent_config.json)
- [setup/agent_setup_notes.md](https://github.com/AndrewConniff/GuitarSales/blob/main/setup/agent_setup_notes.md)

## Cleanup

Remove generated analysis workbooks, briefs, and meeting decks from the demo tenant after delivery if they are no longer needed. Do not add customer confidential information to these public demo artifacts.
