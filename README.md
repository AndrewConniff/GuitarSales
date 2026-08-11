# GuitarSales Agent Chaining Demo for Northstar Acoustic Works

Classification: Public

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this repository.

## Scenario overview

This repository supports a Microsoft 365 Copilot Agents private-delivery demo for a fictional acoustic-instrument manufacturer, **Northstar Acoustic Works**. The scenario is inspired by public themes from guitar manufacturers and music-products industry coverage, then converted into fully synthetic sample data and documents.

Target audience: sales leaders, operations leaders, M365 Copilot champions, and technical sellers demonstrating agent chaining and agent creation.

## Public research basis

- [Martin Guitar public company overview](https://www.martinguitar.com/) - Public inspiration for acoustic craftsmanship, strings, ukulele heritage, player journey positioning, and manufacturing themes.
- [NAMM public news on music-products tariffs](https://www.namm.org/news) - Public inspiration for supply-chain and tariff-risk talking points in the fictional market brief.
- [Music Trades public homepage excerpt](https://musictrades.com/) - Public inspiration for music-products import pressure and tariff uncertainty themes.

No real customer data, private tenant data, internal URLs, or real company metrics are included.

## Technology focus

- Microsoft 365 Copilot prebuilt agents: Analyst agent, Word agent, and PowerPoint agent.
- Custom agent creation in Microsoft 365: SharePoint agent and Copilot chat agent.
- Agent chaining across spreadsheet analysis, executive writing, presentation creation, SOP Q&A, and build-planning Q&A.

## Demo workflow

| Stage | Input | Action | Output |
|---|---|---|---|
| Analyst agent | Regional sales CSV/XLSX files and dashboard template | Create a new workbook from the template and refresh regional analysis | Updated regional sales analysis workbook |
| Word agent | Analysis workbook, sales brief template, public source URLs | Create executive sales brief with market-news context | Sales brief draft |
| PowerPoint agent | Sales brief and deck starter | Create meeting deck | Leadership meeting presentation |
| SharePoint agent | Shop accident SOP | Build SOP Q&A agent and share to Teams group chat | Safety assistant |
| Chat agent | Product build guidelines and wood supplies workbook | Build a material planning assistant | Wood availability and build guidance assistant |

## Repository contents

| File | Purpose | Classification |
|---|---|---|
| `DEMO-INSTRUCTIONS.md` | Presenter guide and all copy/paste prompts | Public |
| `DEMO-INSTRUCTIONS.docx` | Word version of presenter guide | Public |
| `AI-CONTENT-DECLARATION.md` | AI transparency and public-data statement | Public |
| `manifest.json` | Artifact inventory and provenance | Public |
| `sample-data/northeast_regional_sales.csv` | Supporting demo artifact | Public |
| `sample-data/southeast_regional_sales.csv` | Supporting demo artifact | Public |
| `sample-data/midwest_regional_sales.csv` | Supporting demo artifact | Public |
| `sample-data/southwest_regional_sales.csv` | Supporting demo artifact | Public |
| `sample-data/west_regional_sales.csv` | Supporting demo artifact | Public |
| `sample-data/all_regions_sales.csv` | Supporting demo artifact | Public |
| `sample-data/northeast_regional_sales.xlsx` | Supporting demo artifact | Public |
| `sample-data/southeast_regional_sales.xlsx` | Supporting demo artifact | Public |
| `sample-data/midwest_regional_sales.xlsx` | Supporting demo artifact | Public |
| `sample-data/southwest_regional_sales.xlsx` | Supporting demo artifact | Public |
| `sample-data/west_regional_sales.xlsx` | Supporting demo artifact | Public |
| `artifacts/Northstar_Acoustic_Works_Sales_Dashboard_Template.xlsx` | Supporting demo artifact | Public |
| `artifacts/Northstar_Wood_Supplies_Availability.xlsx` | Supporting demo artifact | Public |
| `artifacts/Northstar_Sales_Brief_Template.docx` | Supporting demo artifact | Public |
| `artifacts/Northstar_Shop_Accident_Response_SOP.docx` | Supporting demo artifact | Public |
| `artifacts/Northstar_Product_Build_Guidelines.docx` | Supporting demo artifact | Public |
| `artifacts/Northstar_GuitarSales_Meeting_Deck.pptx` | Supporting demo artifact | Public |
| `setup/sharepoint_safety_agent_config.json` | Supporting demo artifact | Public |
| `setup/chat_build_planning_agent_config.json` | Supporting demo artifact | Public |
| `setup/agent_setup_notes.md` | Supporting demo artifact | Public |

## Download links

- [sample-data/northeast_regional_sales.csv](sample-data/northeast_regional_sales.csv)
- [sample-data/southeast_regional_sales.csv](sample-data/southeast_regional_sales.csv)
- [sample-data/midwest_regional_sales.csv](sample-data/midwest_regional_sales.csv)
- [sample-data/southwest_regional_sales.csv](sample-data/southwest_regional_sales.csv)
- [sample-data/west_regional_sales.csv](sample-data/west_regional_sales.csv)
- [sample-data/all_regions_sales.csv](sample-data/all_regions_sales.csv)
- [sample-data/northeast_regional_sales.xlsx](sample-data/northeast_regional_sales.xlsx)
- [sample-data/southeast_regional_sales.xlsx](sample-data/southeast_regional_sales.xlsx)
- [sample-data/midwest_regional_sales.xlsx](sample-data/midwest_regional_sales.xlsx)
- [sample-data/southwest_regional_sales.xlsx](sample-data/southwest_regional_sales.xlsx)
- [sample-data/west_regional_sales.xlsx](sample-data/west_regional_sales.xlsx)
- [artifacts/Northstar_Acoustic_Works_Sales_Dashboard_Template.xlsx](artifacts/Northstar_Acoustic_Works_Sales_Dashboard_Template.xlsx)
- [artifacts/Northstar_Wood_Supplies_Availability.xlsx](artifacts/Northstar_Wood_Supplies_Availability.xlsx)
- [artifacts/Northstar_Sales_Brief_Template.docx](artifacts/Northstar_Sales_Brief_Template.docx)
- [artifacts/Northstar_Shop_Accident_Response_SOP.docx](artifacts/Northstar_Shop_Accident_Response_SOP.docx)
- [artifacts/Northstar_Product_Build_Guidelines.docx](artifacts/Northstar_Product_Build_Guidelines.docx)
- [artifacts/Northstar_GuitarSales_Meeting_Deck.pptx](artifacts/Northstar_GuitarSales_Meeting_Deck.pptx)
- [setup/sharepoint_safety_agent_config.json](setup/sharepoint_safety_agent_config.json)
- [setup/chat_build_planning_agent_config.json](setup/chat_build_planning_agent_config.json)
- [setup/agent_setup_notes.md](setup/agent_setup_notes.md)

## Setup

1. Download this repository.
2. Upload the files in `artifacts/`, `sample-data/`, and `setup/` to a demo-safe SharePoint location.
3. Use the prompts in `DEMO-INSTRUCTIONS.md` or `DEMO-INSTRUCTIONS.docx`.
4. Do not add customer confidential information to the repository or to generated demo outputs.

## AI transparency

This repository contains AI-generated and human-reviewed demo content. See [AI-CONTENT-DECLARATION.md](AI-CONTENT-DECLARATION.md).

## License

This repository uses the MIT License. See [LICENSE](LICENSE).
