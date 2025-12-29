# Business Insights 360

**Power BI — Executive & Operational Sales, Forecasting and P&L Dashboard**

---

<p align="center">
  <a href="https://app.powerbi.com/view?r=eyJrIjoiNWU0M2Q5YTQtM2ZjNS00NmU0LTg1MzMtNzBhNjYxMzMzZDk1IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9&pageName=ReportSection0e765c0061580b067c73" target="_blank" rel="noopener noreferrer">
    <img
      src="https://img.shields.io/badge/VIEW%20MY%20LIVE%20PROJECT%20%7C%20DEMO-0A66C2?style=for-the-badge&logo=render&logoColor=white"
      alt="View My Live Expense Tracker Project (Live Demo)"
      height="55"
    />
  </a> 

</p>



## Short description

A configurable, interactive Power BI report delivering a 360° view of sales performance, forecast accuracy, product and customer performance, and unit economics. The report is built as a set of reusable visuals and tables that support drill-throughs, cross-filtering and slicer-driven analysis for Finance, Sales, Marketing, Supply Chain and Executive audiences.

This repository contains the project files, sample data schema, and supporting documentation needed to view, refresh and extend the dashboard.

<p align="center">
 <a href="https://drive.google.com/drive/folders/1Wlr4IQ2pHFuXERYyFYWDrjTL9NLhhrT3?usp=drive_link" target="_blank" rel="noopener noreferrer">
    <img
      src="https://img.shields.io/badge/VIEW%20RAW%20DATA%20%7C%20DEMO-0A66C2?style=for-the-badge&logo=render&logoColor=white"
      alt="View Raw Data"
      height="55"
    />
  </a> 
</p>
---

## Table of contents

* [Features](#features)
* [Usage](#usage)
* [Configuration & Data sources](#configuration--data-sources)
* [Development notes](#development-notes)
* [Contributing](#contributing)
* [Roadmap](#roadmap)
* [License](#license)

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

## License

```
MIT License — see LICENSE file in this repository.
```

### Contact

<p align="center">
 <!-- Contact & Immediate Reach -->
<a href="mailto:ajithramesh2020@gmail.com">
  <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

<a href="tel:+919345264522">
  <img src="https://img.shields.io/badge/Call%20Me-0A66C2?style=for-the-badge&logo=phone&logoColor=white"/>
</a>

<a href="https://wa.me/9345264522">
  <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/>
</a>

<!-- Professional Identity -->
<a href="https://www.linkedin.com/in/ajith-ramesh-data-analyst/">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://ajith-data-analyst.github.io/Portfolio/Ajith_R_Resume.pdf">
  <img src="https://img.shields.io/badge/Resume-4CAF50?style=for-the-badge&logo=googledrive&logoColor=white"/>
</a>

<!-- Work Proof -->
<a href="https://ajith-data-analyst.github.io/Portfolio/home.html">
  <img src="https://img.shields.io/badge/Portfolio-FF6B6B?style=for-the-badge&logo=web&logoColor=white"/>
</a>

<a href="https://github.com/Ajith-data-analyst">
  <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white"/>
</a>
</p>
---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer"/>
</p>

