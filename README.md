📈 Big Tech Stock Market Analysis Dashboard | Power BI Project

Markets move fast — but insights shouldn’t lag behind.
I designed this Stock Market Analysis Dashboard in Power BI to track and compare how major tech companies perform across price, volume, and long-term momentum.
What started as raw CSVs of daily stock data evolved into a dynamic visualization tool that tells a decade-long story of innovation, volatility, and growth.

🎯 Purpose & Business Context

Financial analysts and investors constantly juggle multiple tickers, timeframes, and KPIs.
The challenge I wanted to solve was:

“Can we visually decode which companies truly lead the tech sector — not only by share price but by sustained market participation?”

The dashboard serves as a performance and volume intelligence system:

Tracks year-wise closing prices and trading volumes.

Compares stock symbols side-by-side for trend correlation.

Calculates average close, highest/lowest price, and total volume traded.

Highlights the strongest performers through custom DAX ranking.

🧩 Data Model & Preparation
File	Description
big_tech_stock_prices.csv	Historical daily price & volume data for top technology companies.
big_tech_companies.csv	Company metadata (symbol, sector, headquarters).
big_tech_stock_prices.Pivot_Table.csv	Aggregated summary for faster visualization.
Stock.Market.Dashboard.pbix	Final Power BI report with relationships, DAX measures, and visuals.
Stock Analysis Dashboard.png	Final dashboard preview.
🔧 Transformation Workflow (Power Query)

Cleaned and standardized date formats, ensuring chronological consistency.

Removed nulls and anomalies in closing prices & volumes.

Added calculated columns for Year, Month, and Quarter.

Merged company metadata with pricing data for contextual visuals.

Aggregated totals for YoY comparison and forecasting base.

⚙️ Tech Stack

Power BI Desktop – dashboarding and DAX modeling

Power Query (M) – ETL for CSV transformations

DAX – custom measures for price aggregation, averages, and ranking

Excel / CSV – raw data source

📊 Dashboard Overview
KPI	Value / Insight
Total Volume	≈ 2 Trillion shares traded (2010-2023)
Lowest Price	1 USD – historic low baseline
Highest Price	700.99 USD – peak close (AMZN 2021)
Average Close Price	89.27 USD across tickers
Key Insights

📈 AAPL & AMZN dominate both price growth and trading activity.

🟣 META & NFLX show aggressive peaks during digital-boom years.

🟢 ADBE & CRM illustrate steady compounding rather than volatility.

🔻 Volume trends reveal post-2021 contraction as markets normalized.

🧮 DAX Logic
Calculation	Formula / Concept
Average Close Price	AVERAGE('Prices'[close])
Total Volume	SUM('Prices'[volume])
Highest Price	MAX('Prices'[close])
Lowest Price	MIN('Prices'[close])
Performance Rank	RANKX(ALL('Companies'), [Average Close Price], , DESC)
Volume vs Price Correlation	Scatter plot of SUM(close) vs SUM(volume) for each ticker
🔮 Forecast & Trend Interpretation

Rather than relying on static KPIs, I layered a Power BI forecasting visual (exponential smoothing) to identify:

Long-term upward drift for cloud-based companies.

Short-term volatility spikes aligning with major product releases and market events.

A flattening trajectory in 2022–2023 indicating market saturation in legacy players.

This trend insight turns historical data into a forward-looking view of sector momentum.

🖥️ Dashboard Features

1️⃣ Stock Price Trends – Multi-line chart of closing prices (2010–2023).
2️⃣ Volume Trends – Yearly trading volume comparison.
3️⃣ Volume vs Price Scatter – Identifies liquidity vs. valuation strength.
4️⃣ Volume Comparison Bar – Ranks companies by overall market activity.
5️⃣ Performance Comparison – Average closing price leaderboard for visual benchmarking.

🧠 What I Learned

Structuring financial data for time-series analytics in Power BI.

Building multi-table relationships for ticker-level drilldowns.

Creating a high-contrast dark-to-neon gradient theme for better readability and brand distinction.

Integrating both descriptive (KPI) and diagnostic (volume vs price) analytics in one interface.

Communicating financial insights visually—bridging quant analysis and storytelling.
