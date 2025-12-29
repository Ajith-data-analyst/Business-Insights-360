# Business Insights 360

**Power BI — Executive & Operational Sales, Forecasting and P&L Dashboard**

---

## Short description

A configurable, interactive Power BI report delivering a 360° view of sales performance, forecast accuracy, product and customer performance, and unit economics. The report is built as a set of reusable visuals and tables that support drill-throughs, cross-filtering and slicer-driven analysis for Finance, Sales, Marketing, Supply Chain and Executive audiences.

This repository contains the project files, sample data schema, and supporting documentation needed to view, refresh and extend the dashboard.

> Status: **Work in Progress / Proof of Concept** — update the files and `README` after major releases.

---

## Table of contents

* [Demo / Screenshots](#demo--screenshots)
* [Features](#features)
* [Repository contents](#repository-contents)
* [Prerequisites](#prerequisites)
* [Installation & Open](#installation--open)
* [Usage](#usage)
* [Configuration & Data sources](#configuration--data-sources)
* [Development notes](#development-notes)
* [Contributing](#contributing)
* [Roadmap](#roadmap)
* [FAQ](#faq)
* [License](#license)

---

## Demo / Screenshots

Screenshots show the core report pages (Executive overview, Forecast accuracy, Product performance, Unit economics and Landing page). Screenshots are stored in `/docs/screenshots/`.

* `docs/screenshots/dashboard-landing.png` — Landing page and navigation.
* `docs/screenshots/overview.png` — Executive KPI tiles and division/channel charts.
* `docs/screenshots/forecast-accuracy.png` — Forecast accuracy and net error trend.
* `docs/screenshots/product-performance.png` — Product and region performance matrix.

*(Each image includes descriptive alt text for accessibility.)*

---

## Features

* Executive overview with KPI tiles (Net Sales, GM%, Forecast Accuracy, Net Profit%).
* Forecast accuracy and net error trend analysis by customer/product/time.
* Product performance tables and a performance matrix (unit economics vs net profit %).
* Customer and product leaderboards (Top/Bottom by revenue and P&L impact).
* Unit economics visualization (COGS, gross margin, operational expense waterfall).
* Slicer-driven regional / market / customer / segment filters and quarter/year selectors.
* Export-ready numbers and copy-paste friendly P&L table.

---

## Repository contents

```
/ (root)
├─ Business-Insights-360.pbix        # Power BI Desktop report file (primary deliverable)
├─ data/                             # sample or extract CSVs used for building visuals
│  ├─ sales.csv
│  └─ customers.csv
├─ docs/
│  └─ screenshots/                   # exported dashboard screenshots (recommended)
├─ README.md                         # this file
└─ LICENSE                           # project license (add or update)
```

> If your repo differs, update this section so the README matches reality.

---

## Prerequisites

* **Power BI Desktop** (recommended) — match the version used to build the `.pbix` (if unknown, use latest stable Power BI Desktop).
* Windows or a compatible OS that runs Power BI Desktop.
* If using DirectQuery or database sources: credentials and network access to the data sources.

---

## Installation & Open

1. Clone the repository:

```bash
git clone https://github.com/<your-org>/business-insights-360.git
cd business-insights-360
```

2. Open `Business-Insights-360.pbix` in Power BI Desktop.
3. If prompted, update data source credentials (see Configuration section).

All commands are copy-paste safe.

---

## Usage

* Use the top navigation icons to switch pages (Landing, Sales, Forecast, Products, Unit Economics, Executive).
* Apply slicers at the top for `year`, `quarter`, `region`, `customer`, and `segment`.
* Interact with charts: click a bubble/segment to cross-filter related visuals.
* Export data from any visual via the visual menu (ellipsis → Export data) for offline analysis.

Expected outputs: interactive report views and exportable CSVs for visuals.

---

## Configuration & Data sources

* Local CSVs are under `/data/` for development and testing.
* Production datasets should be configured as either:

  * Scheduled refresh to an Azure SQL / SQL Server / Snowflake / other warehouse, or
  * Power BI Gateway (on-premises) + scheduled refresh.
* **Environment variables / secrets:** do not store secrets in the repo. Use Power BI service credentials and the gateway for production refresh.

**Important:** Update connection strings and credentials before scheduling refresh.

---

## Development notes

* Visuals use a combination of DAX measures and calculated columns.
* Keep visual-level formatting separate from data model logic — amend measures in the *Model* view.
* When adding new measures, include a short description and expected sample results in the measure name or a supporting documentation file.

If a visual breaks after changes, verify data types and time-intelligence relationships.

---

## Contributing

Contributions are welcome. Please follow these steps:

1. Fork the repository.
2. Create a branch: `feature/<short-desc>`.
3. Add your PBIX or incremental model changes and a brief note describing the change.
4. Submit a pull request describing the purpose and verification steps.

If you expect to modify the data model, open an issue first so we can coordinate model-level changes.

---

## Roadmap

* [ ] Add bookmark-driven storytelling (monthly exec deck)
* [ ] Implement row-level security for regional executives
* [ ] Add automated ETL scripts to generate the development CSVs
* [ ] Publish a data dictionary and measure catalogue

---

## FAQ

**Q:** Which Power BI version was used to build this report?
**A:** The original build was done with Power BI Desktop (report author should add exact version). If unsure, open in the latest Power BI Desktop and update model where required.

**Q:** Are the figures in USD or local currency?
**A:** Values are shown as dollars and millions — verify currency in model if using alternate currency.

---

## License

Specify the project license here and ensure a matching `LICENSE` file is added to the repository. Example placeholder:

```
MIT License — see LICENSE file in this repository.
```

If no license is intended, explicitly mark the code `Copyright (c) <year> <owner>` and add a `LICENSE` stating restrictions.

---

## Professional checklist (before publishing)

* [ ] A new user can open and view the report with only Power BI Desktop.
* [ ] All commands in this README are copy-paste safe.
* [ ] No private keys or credentials in the repo.
* [ ] Screenshots are up to date and located in `/docs/screenshots/`.
* [ ] LICENSE file present and matches README statement.

---

### Contact

Ajith — maintainer
Email / LinkedIn: update contact details in the repo's `CONTRIBUTING.md` if you want contributor outreach to be direct.

*Generated to follow the GitHub README Rules & Best Practices provided. Replace placeholders (license, exact Power BI version, contact email) before publishing.*
