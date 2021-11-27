# Income statement API on https://site.financialmodelingprep.com.
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
symbol : Company Symbol, ex. AAPL
companyCik : Number
reportingCik : Number
limit : Number
```

