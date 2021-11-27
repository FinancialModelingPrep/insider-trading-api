# [Income Statement API Documentation](https://site.financialmodelingprep.com/docs)
That describes how to use insider trading API on financialmodelingprep.com. 
<br />
<br />
**GET YOUR APIKEY IN SECOND ON https://site.financialmodelingprep.com/developer**
<br />
<br />
The federal securities laws require certain individuals (such as officers, directors, and those that hold more than 10% of any class of a company’s securities, together we’ll call, “insiders”) to report purchases, sales, and holdings of their company’s securities by filing Forms 3, 4, and 5.
<br />
Each item returned from the endpoint also has a price field, which indicates what price this transaction was filed at. The price can be 0 if the company gave them stocks or options.
<br />

**Documentaion:** https://site.financialmodelingprep.com/developer/docs/stock-insider-trading
<br />

**Request Parameters:**

```solidity
String symbol : ex. AAPL
Integer companyCik : ex. 0000320193
Integer reportingCik : ex. 0000320193
Integer limit : ex. 120
```

**Request Examples:** <br />
Most recent Stock Insider trading Transaction: <br />
https://financialmodelingprep.com/api/v4/insider-trading?transactionType=P-Purchase,S-Sale&limit=100&apikey=YOUR_API_KEY <br />

Stock insider trading using ticker: <br />
https://financialmodelingprep.com/api/v4/insider-trading?symbol=AAPL&limit=100&apikey=YOUR_API_KEY <br />

Stock insider trading using reporting CIK: <br />
https://financialmodelingprep.com/api/v4/insider-trading?reportingCik=0001663020&limit=100&apikey=YOUR_API_KEY <br />

Stock insider trading using company CIK: <br />
https://financialmodelingprep.com/api/v4/insider-trading?companyCik=0000320193&limit=100&apikey=YOUR_API_KEY <br />
<br />

Also you can get the list of all transaction types: <br />
https://financialmodelingprep.com/api/v4/insider-trading-transaction-type?apikey=YOUR_API_KEY <br />
<br />

**Response Example:**
```json
[
  {
    "symbol" : "AAPL",
    "transactionDate" : "2021-02-02",
    "reportingCik" : "0001214128",
    "transactionType" : "S-Sale",
    "securitiesOwned" : 4532724,
    "companyCik" : "0000320193",
    "reportingName" : "LEVINSON ARTHUR D",
    "acquistionOrDisposition" : "D",
    "formType" : "4",
    "securitiesTransacted" : 3416,
    "securityName" : "Common Stock",
    "link" : "https://www.sec.gov/Archives/edgar/data/0000320193/000032019321000023/0000320193-21-000023-index.htm"
  }, {
    "symbol" : "AAPL",
    "transactionDate" : "2021-02-01",
    "reportingCik" : "0001051401",
    "transactionType" : "M-Exempt",
    "securitiesOwned" : 0,
    "companyCik" : "0000320193",
    "reportingName" : "JUNG ANDREA",
    "acquistionOrDisposition" : "D",
    "formType" : "4",
    "securitiesTransacted" : 3416,
    "securityName" : "Restricted Stock Unit",
    "link" : "https://www.sec.gov/Archives/edgar/data/0000320193/000032019321000022/0000320193-21-000022-index.htm"
  },
]
```
