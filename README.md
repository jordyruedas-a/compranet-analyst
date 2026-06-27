# 🇲🇽 Mexican Public Procurement Analytics (Compranet Historical Dataset)

**Author:** Jordan Emanuel Ruedas Vázquez  
**Project Type:** Data Science / Business Intelligence Portfolio  
**Core Technologies:** Python (Pandas, NumPy, Matplotlib, Seaborn), Jupyter Notebook, Microsoft Power BI (for visualization)  
**Dataset:** Mexican Government Open Data (Compranet Historical System 2010–2022)  
**File Size:** ~907 MB (CSV)  

---

## 📋 Executive Summary

This project demonstrates a complete end-to-end data analysis workflow using real-world Mexican government procurement data from the **Compranet** historical system (2010–2022). 

The primary objective was to transform a massive, raw CSV dataset (over 900 MB) into clean, structured data and actionable business insights. By leveraging Python for data wrangling and exploratory analysis, I extracted Key Performance Indicators (KPIs) that reveal spending patterns, top suppliers, and seasonal trends in public contracting. 

The final output includes a clean dataset ready for analysis and a pre-calculated metrics file designed to feed directly into a **Microsoft Power BI** dashboard for executive visualization.

---

## 🎯 Business Problem & Data Context

Public contracting data is often fragmented and difficult to analyze due to its size, inconsistent formatting, and lack of real-time integration. This project addresses the need for transparency and efficiency in analyzing public spending.

**Key challenges addressed:**
- Cleaning and standardizing supplier names to avoid duplicates.
- Converting string-based monetary values into numerical floats for aggregation.
- Parsing non-standard date formats to enable time-series analysis.
- Filtering and grouping data to identify top spenders and procedural trends.

---

## 🛠️ Technical Process & Methodology

### 1. Data Ingestion & Optimization (Python / Pandas)
- Loaded a ~907 MB CSV file using `pd.read_csv` with memory optimization (`usecols` to load only relevant columns).
- Parsed date columns (`fecha_inicio`, `fecha_fin`) into `datetime` objects for time-based analysis.
- Handled mixed data types and missing values through targeted imputation and filtering.

### 2. Data Cleaning & Feature Engineering
- **Text Normalization:** Converted supplier names and contracting entities to uppercase and stripped whitespace to ensure accurate aggregation (`groupby`).
- **Currency Filtering:** Isolated contracts denominated in Mexican Pesos (`MXN`) to ensure monetary consistency.
- **Temporal Features:** Engineered new columns for `Year` and `Month` extracted from the start date to analyze seasonality and annual trends.

### 3. Key Performance Indicators (KPIs) Extraction
Using `pandas` `groupby` and `agg` functions, the following core metrics were calculated and exported:
- **Annual Total Spending:** Sum of contract amounts aggregated by fiscal year.
- **Annual Contract Count:** Volume of public procurement events per year.
- **Average Contract Amount:** Mean value of contracts per year (to gauge inflation or budget shifts).
- **Top 10 Suppliers:** The highest-earning vendors by total contract value.
- **Monthly Spending Trends:** Identification of peak spending months (e.g., end-of-year budget execution).

### 4. Data Visualization (Matplotlib / Seaborn)
Four core visualizations were generated to communicate findings:
1.  Evolution of Annual Public Spending (Line Chart).
2.  Top 10 Suppliers by Total Contract Value (Bar Chart).
3.  Average Contract Value per Year (Bar Chart).
4.  Number of Contracts per Year (Bar Chart).

---

## 📊 Power BI Dashboard Integration *(Placeholder)*

The final step of this project is the creation of an interactive dashboard in **Microsoft Power BI**. 

This dashboard utilizes the `compranet_limpio.csv` for granular filtering and the `kpis_compranet.csv` for high-level executive summaries. 

**[🔗 Link to Live Power BI Dashboard]**  
*Please insert your Power BI public link here when available.*

---

## 📁 Repository Structure
/ (Root)
├── Analisis_Compranet.ipynb # Full Python analysis code (Jupyter Notebook)
├── compranet_historico.csv # Original raw dataset (1 GB - required for execution)
├── compranet_limpio.csv # Clean, filtered dataset ready for Power BI
├── kpis_compranet.csv # Pre-calculated aggregated metrics for dashboards
├── graficos_kpis.png # Generated static visualizations from Python
├── README.md # This file (Project documentation)
└── output_graficas/ # (Optional folder containing individual chart PNGs)



---

## 🚀 How to Run This Project

1.  **Clone the repository** to your local machine.
2.  Ensure you have the required Python libraries installed:
    ```bash
    pip install pandas numpy matplotlib seaborn

    Open Analisis_Compranet.ipynb in Jupyter Notebook or VS Code.

    Execute all cells (Kernel -> Restart & Run All).

    The script will generate compranet_limpio.csv, kpis_compranet.csv, and graficos_kpis.png in the project folder.

📈 Key Findings & Insights

    Budget Execution Trends: Significant spikes in public spending are observed in the final months of the fiscal year, indicating accelerated budget execution.

    Market Concentration: The top 10 suppliers account for a significant percentage of total contract value, suggesting a concentration of public procurement among a few key vendors.

    Procurement Methods: Adjudicaciones directas (direct awards) represent a large portion of the contract count, highlighting the dominance of simplified bidding procedures.

📬 Contact & Portfolio

Author: Jordan Emanuel Ruedas Vázquez
LinkedIn: [Your LinkedIn Profile Link Here]
GitHub: [Your GitHub Profile Link Here]

This project was developed as part of a Data Science and Business Intelligence portfolio to demonstrate proficiency in Python, data cleaning, and analytical thinking using open government data.



---

### 📌 Últimas instrucciones para dejarlo perfecto:

1. **Crea el archivo:** En tu VS Code, crea un archivo nuevo llamado `README.md` (exactamente así). Pega todo el código que te di.
2. **Guarda el archivo** (Ctrl+S).
3. **Lo que tienes que llenar tú:**
   - Cuando hagas tu dashboard en Power BI y lo publiques a la nube (Power BI Service), **copia el enlace público y pégalo donde dice `[🔗 Link to Live Power BI Dashboard]`**.
   - Agrega tus enlaces reales de LinkedIn y GitHub al final del documento.
4. **Sube todo a GitHub:** Sube la carpeta completa con el Notebook, los archivos CSV generados, el `README.md` y la imagen `graficos_kpis.png`.

¡Tu portafolio ahora es de primer nivel! Cuando subas el dashboard a Power BI, no olvides actualizar el README con el enlace. Si tienes dudas al subir el dashboard o al hacer el commit en GitHub, aquí estoy. ¡Mucho éxito!

