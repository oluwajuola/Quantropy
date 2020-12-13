# Quαntropy

The human mind is fascinating. Give it a series of observations, and it will attempt to find structure to it. 
It will find variables upon which the given data might depend on, and develop elaborate models, 
in the hopes of predicting future observations. What if this search for the Holy Grail is all in vain? 
What if we have been fooled by randomness? 

## Framework Description

This project is an attempt to shed light on this question that has puzzled researchers for the past century. It is the culmination of three years of learning about the financial markets, and almost a year of
developing a platform in order to provide a comprehensive and unified approach to trading the financial markets.

We replicate the research and industry methodologies that have been used in order to allow our community to
more flexibly validate them *ex-post*, reuse, and extend on. The pipeline looks as such:

1.  In the `historical_data_collection` package, we scrape data from various sources, including SEC Edgar for **financial statements** and **market classification**,
    YahooFinance for **asset prices**, Fred for **macroeconomic data**, and Fama-French for **risk factors**. 
    *Currently migrating from Excel and Pickle files to MongoDB and Kafka for real-time streaming.*

2.  a.  In the `fundamental_analysis` package, we provide tools to assess a company's fair value (**equity valuation models**),
        and evaluate by looking at **accounting ratios** and accompanying *financial distress* and *earnings manipulation* models,
        and compare across time and competitors. 
    
    b. In the `technical_analysis` package, we provide tools to detect geometric shapes (**chart patterns**, **candlestick patterns**) 
    and price characteristics (**technical indicators**). *Still under development, not a priority, but can use `TA-Lib` meanwhile.*
    
    c. In the `quantitative_analysis` package, we provide tools to study statistical characteristics of stocks for **risk quantification**,
    **stochastic processes**.
    
3.  In the `portfolio_management` package, we construct portfolios by using the aforementioned analysis for **stock screening**, as well as quantitative techniques for **asset pricing modeling**
    and **portfolio optimization**. We can then backtest the strategy using the **portfolio simulator**, and deploy it to a broker.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Current opportunities for contribution include:

* **Documentation**: For literally everything. 
* **Data collection**: Scraping *alternative data* (news sentiment analysis, web/app usage and reviews etc.), improve the *HTML scraper* for Edgar.
* **Fundamental analysis**: Using `matplotlib` for appropriate visualizations across time, industry, sector, and market.
* **Portfolio management**: Implementing risk parity models for portfolio optimization, and pre-defined strategies of 
superinvestors (i.e. Warren Buffet, Benjamin Graham, Peter Lynch) based on books written and interviews. Extending broker deployment implementation.

Please make sure to update tests as appropriate.

## License

MIT License

Copyright (c) 2020 Alain Daccache

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.