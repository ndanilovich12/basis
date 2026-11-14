# Bull Run

Market analysis and business analytics that run in the browser. Part of my portfolio site: https://smallmarketsoftwares.netlify.app/lab.html

## What it does

**Markets**

- Real daily closing prices for 14 large US stocks (Apple, Microsoft, Nvidia, Alphabet, Amazon, Meta, Tesla, AMD, Broadcom, Netflix, Oracle, Salesforce, JPMorgan, Costco) plus the Nasdaq-100 (QQQ) and S&P 500 (SPY) ETFs
- 20-day and 50-day moving averages, Bollinger bands and RSI
- The biggest one-day gains and drops, marked on the chart and sized against a normal day
- Return, annualized volatility, maximum drawdown, return per unit of risk and beta to the S&P 500
- A compare view, a correlation grid, and a short written read of the numbers
- On the live site, any ticker can be added from a search box

**Portfolio**

- Set weights, then backtest them on real prices: growth of $10,000 against the S&P 500
- Volatility, drawdown, beta, and how much each holding added or cost
- Presets: equal weight, big tech, chips, defensive

**Business**

- Drop in a sales or orders CSV. It finds the date, the measure and the categories on its own.
- Monthly trend with a projection, a breakdown by category and a day-of-week pattern
- What-if sliders for price, volume and cost against the projection
- Written takeaways, each with the formula behind it

## How it is built

Plain HTML, CSS and JavaScript. No frameworks, no chart library and no build step.

- `index.html` is the page and its interface code
- `lab-core.js` holds the statistics, the CSV parser and the SVG charts
- `tech-data.js` is a saved price history from Yahoo Finance (November 13, 2026)

To run it, open `index.html` in a browser.

## Notes

- Here the stock prices are a saved snapshot. On my site the page refreshes them and supports ticker search through a small proxy rule.
- The takeaways are rule-based. No language model is involved.
- Uploaded files are read in the browser and never sent anywhere.
- This describes past data. It is not investment advice.
