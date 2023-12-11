# TradingView PineScript v5 Boilerplate Template
A **simple** boilerplate starter template for your pine script coding.

## Features
* **Safety** - Max Drawdown Total (Cash & Acc. Equity %)
* **Safety** - Max Drawdown Day (Cash & Acc. Equity %)
* **Safety** - Max Loss No. Days
* **Safety** - Daily orders
* **Safety** - Max Contracts
* **Restrictions** - Backtest Range
* **Restrictions** - Hours Range (No Nights)
* **Risk** - Anti-News Trading
* **Risk** - Wait No. candles after loss 
* **Trading** - Take Profit / Stop Loss
* **Trading** - Recent High/Low with Risk Reward Ratio
* **Trades** - Only Buy or Sell Option
* **Trades** - Reverse Buy & Sell Entry
* **Highlight** - Outside backtest times
* **Highlight** - Outside trading times


## Instructions
1. Run code and see if it works out of the box!

2. Review the first 4 lines and edit the `strategy` options as this may **override** any custom coding you do and GUI options set.

3. Anything between the EDIT tags is for your custom code, sample code displayed there.

```
///////////////////////////////////////////////
//                                           //
//    EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT  ⇣     //
//                                           //
///////////////////////////////////////////////

//             [ Your Code Here ]

///////////////////////////////////////////////
//                                           //
//    EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT  ⇡     //
//                                           //
///////////////////////////////////////////////
```

4. Take note of the variables `usr_logic_buy` and `usr_logic_sell` within the EDIT section. When true, trades will be triggered in that respective direction.

```
if usr_logic_ema_buy == true
    usr_logic_buy := true

if usr_logic_ema_sell == true
    usr_logic_sell := true
```

5. Reset your variables at the very bottom of the script. 

6. Happy trading!

## Example
A simple working example of some custom code in an organised fashion, also included in example script.

```
////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//                                                                                                                    //
//      EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT  ⇣   EDIT  ⇣  EDIT  ⇣  EDIT  ⇣  EDIT      //
//                                                                                                                    //
////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

// === USER STRATEGY ===

// Variables
var usr_logic_ema_buy  = false
var usr_logic_ema_sell = false

// Input
usr_input_ema_length   = input.int(9, step=1, title="EMA Length", group="User Strategy")
usr_input_ema_diff     = input.float(0.5, step=0.1, title="EMA Above/Below Pips", group="User Strategy")

// Function
usr_funct_ema          = ta.ema(close, usr_input_ema_length)

// Logic
if close > (usr_funct_ema + (usr_input_ema_diff/10000))      // 3 Pips Above EMA then Sell (Reversal)
    usr_logic_ema_sell := true

if close < (usr_funct_ema - (usr_input_ema_diff/10000))      // 3 Pips Below EMA then Buy (Reversal)
    usr_logic_ema_buy := true

// Plot
plot(usr_funct_ema, color=color.yellow, title="EMA")

// Decision
if usr_logic_ema_buy == true
    usr_logic_buy := true

if usr_logic_ema_sell == true
    usr_logic_sell := true

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//                                                                                                                    //
//      EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT  ⇡   EDIT  ⇡  EDIT  ⇡  EDIT  ⇡  EDIT      //
//                                                                                                                    //
////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
```

## Variable Guide
Please continue the use of these variable formatting prefixes to keep your code organised.

### Prefixes (Level 1)
 - **sys_** = Template Variables
 - **usr_** = User Variables (Your Custom)

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

## Todo
* Consolidation and Trending Market Trade Switches
* Add additional simple examples to readme
* Determine if there is other ways to detect news
* Trailing Stop Loss
* Webhook Alerts

## Disclaimer
The Pine Script code provided in this repository is for educational and informational purposes only. It is not intended as financial or investment advice and should not be construed as such. Trading and investing in financial markets involve risk, and past performance is not indicative of future results.

The author of this code is not a financial advisor, and no content in this repository should be considered as professional financial advice. You should seek the advice of a qualified professional for any financial decisions.

The author makes no representations or warranties regarding the accuracy, completeness, or suitability of the code provided. The code is provided "as is," and the author disclaims any liability for any losses, damages, or injuries arising from its use.

Trading and investing involve substantial risk, and you should carefully consider your financial situation and consult with a qualified professional before making any investment decisions.

By using or adapting the code in this repository, you agree to release the author from any and all liability associated with the use of the code. The author is not responsible for any direct, indirect, or consequential damages resulting from the use of the code.

Use this code at your own risk, and only after thorough testing in a simulated environment. Always practice responsible risk management and make informed decisions based on your own research and judgment.

## Author
[https://github.com/sysvar/pine-script-template]
