# TradingView PineScript v5 Boilerplate Template
A simple boilerplate starter template for your pine script coding.

## Features
* Safety - Max Drawdown
* Safety - Max Contracts
* Safety - Max Loss No. Days
* Restrictions - Backtest Range
* Restrictions - Hours Range (No Nights)
* Restrictions - Anti-News Trading
* Trades - Take Profit/Stop Loss
* Trades - Only Buy/Sell
* Trading - Take Profit / Stop Loss


## Instructions
1. Run code and see if it works out of the box!

2. Review the first 10 lines and edit the `strategy` options and `strategy.risk` safety features as this will **override** any custom coding you do and GUI options set.

3. Anything between the EDIT tags is for your custom code, sample code displayed there.

```
///////////////////////////////////////////////
//                                           //
//    EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT  ⇣   //
//                                           //
///////////////////////////////////////////////

//             [ Your Code Here ]

///////////////////////////////////////////////
//                                           //
//    EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT  ⇡   //
//                                           //
///////////////////////////////////////////////
```

4. Take note of the `// === USER FINAL LOGIC ===` within the EDIT section. When variables `sys_logic_buy` and `sys_logic_sell` are true, trades will be triggered. 

5. That should be it, happy trading!

## Variable Guide
Please continue the use of these variable formatting prefixes to keep your code organised.

### Prefixes (Level 1)
 - **sys_** = Template Variables
 - **usr_** = Your Custom User Variables

### Prefixes (Level 2)
 - \*\*\*_**input**\_ = For Editable GUI Inputs
 - \*\*\*_**funct**\_ = For Indicators/Functions
 - \*\*\*_**logic**\_ = For Math/Calulations

### Prefixes (Level 3)
 - \*\*\*_\*\*\*\*\*\_**backtest**\_ = Category Example 1
 - \*\*\*_\*\*\*\*\*\_**time**\_ = Category Example 2

### Prefixes (Level 4)
 - \*\*\*_\*\*\*\*\*\_backtest\_**start** = Category Item Example 1
 - \*\*\*_\*\*\*\*\*\_backtest\_**end** = Category Item Example 2


## Disclaimer
The Pine Script code provided in this repository is for educational and informational purposes only. It is not intended as financial or investment advice and should not be construed as such. Trading and investing in financial markets involve risk, and past performance is not indicative of future results.

The author of this code is not a financial advisor, and no content in this repository should be considered as professional financial advice. You should seek the advice of a qualified professional for any financial decisions.

The author makes no representations or warranties regarding the accuracy, completeness, or suitability of the code provided. The code is provided "as is," and the author disclaims any liability for any losses, damages, or injuries arising from its use.

Trading and investing involve substantial risk, and you should carefully consider your financial situation and consult with a qualified professional before making any investment decisions.

By using or adapting the code in this repository, you agree to release the author from any and all liability associated with the use of the code. The author is not responsible for any direct, indirect, or consequential damages resulting from the use of the code.

Use this code at your own risk, and only after thorough testing in a simulated environment. Always practice responsible risk management and make informed decisions based on your own research and judgment.

## Author
[https://github.com/sysvar/pine-script-template]
