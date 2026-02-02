# Algolia Single Query Usage Analyzer

Visualize Algolia search request volumes per index over time with Chart.js.

**🔗 Tool:** [emirbelkahia.github.io/algolia-single-query-usage-analyzer](https://emirbelkahia.github.io/algolia-single-query-usage-analyzer/)

> **⚠️ Important Limitation:** This tool only tracks **single query traffic**. Multi-query traffic (which can target multiple indices simultaneously and counts as 1 operation in Algolia billing) cannot be accurately attributed to specific indices and is therefore excluded. This tool is **only useful for applications using primarily single queries** — for most Algolia implementations with multi-query traffic, this provides an incomplete view of per-index usage.

## What it does

This web-based tool fetches search request data from the Algolia Usage API and displays it as an interactive bar chart. It helps visualize which indices generate the most API traffic over a specified time period.

**Key features:**
- Fetch usage data for multiple indices at once
- Visualize data as a Chart.js bar chart
- Download chart as PNG
- Query suggestion counts automatically subtracted for accuracy

## Use Cases

**Best for:**
- Applications using primarily single queries (not multi-queries)
- Quick per-index usage overview
- CS/Operations teams monitoring API consumption

**Not suitable for:**
- Applications with significant multi-query traffic (most modern implementations)
- Precise quota attribution across all indices

## How to Use

1. **Access the tool:** Visit [emirbelkahia.github.io/algolia-single-query-usage-analyzer](https://emirbelkahia.github.io/algolia-single-query-usage-analyzer/)

2. **Enter your credentials:**
   - Algolia Application ID
   - Algolia Usage API Key (requires paid account with quota access)
   - Number of days (max 90)
   - Comma-separated list of indices

3. **Generate chart:**
   - Submit the form to fetch and visualize data
   - Optionally download the chart as PNG

**Tip:** Save your comma-separated index list in a text file for quick copy/paste on repeat use.

## Technical Details

- **Frontend only:** Pure JavaScript, runs entirely in the browser
- **No backend:** API keys stay in your browser
- **Chart.js:** For data visualization
- **Data processing:** Query suggestions are subtracted from total search requests for accuracy

## Limitation Details

Algolia's billing model counts multi-queries as a single operation, even when targeting multiple indices. Since multi-query traffic cannot be precisely attributed to individual indices, this tool only analyzes single-query traffic. For applications with heavy multi-query usage, the data shown here will be incomplete.

## About

Built by [Emir Belkahia](https://www.linkedin.com/in/emirbelkahia/), Customer Success Manager at Algolia, in 2024.

Not an official Algolia product.

## License

MIT License
