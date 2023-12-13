# Royal Scalping Indicator M4

This is a custom indicator for MetaTrader 5 (MQL5) developed by Forex Robot Easy Team. It is designed to provide high-quality trading signals for scalping strategies. The indicator uses two oscillators, a trend oscillator and a signal oscillator, to identify potential trend reversals and generate buy or sell signals accordingly.

## Input Parameters

- **EnableSoundAlerts**: This parameter enables or disables sound alerts for buy and sell signals. By default, it is set to true.
- **EnablePushNotifications**: This parameter enables or disables push notifications for buy and sell signals. By default, it is set to true.
- **EnableFlashingSignals**: This parameter enables or disables flashing signals on the chart when a trend reversal is detected. By default, it is set to true.
- **TrendOscillatorPeriod**: This parameter sets the period for the trend oscillator. By default, it is set to 14.
- **SignalOscillatorPeriod**: This parameter sets the period for the signal oscillator. By default, it is set to 9.
- **RiskPercentage**: This parameter sets the risk percentage for position sizing. By default, it is set to 2.

## Global Variables

- **trendOscillatorHandle**: This variable holds the handle for the trend oscillator indicator.
- **signalOscillatorHandle**: This variable holds the handle for the signal oscillator indicator.
- **lotSize**: This variable holds the lot size for trading based on the risk percentage.

## Indicator Initialization

The `OnInit()` function is called during indicator initialization. It creates the trend oscillator and signal oscillator using the `iCustom()` function. It also calculates the lot size based on the account balance and risk percentage.

## Indicator Deinitialization

The `OnDeinit()` function is called during indicator deinitialization. It deletes the trend oscillator and signal oscillator objects using the `ObjectDelete()` function.

## Indicator Calculation

The `OnCalculate()` function is called during each iteration of the indicator. It calculates the current values of the trend oscillator and signal oscillator using the `iCustom()` function. It then checks for trend reversals and generates buy or sell signals accordingly. If a trend reversal is detected and `EnableFlashingSignals` is true, a flashing signal is displayed on the chart using the `ObjectCreate()` and `ObjectSetText()` functions. Buy or sell orders are placed using the `OrderSend()` function.

## Push Notification Function

The `SendNotification()` function is a custom function used to send push notifications. It takes a message as an input parameter and sends it as a push notification using the `NotificationsSend()` function.

Please note that Forex Robot Easy Team is not the official developer of this product. This code is only a sample that can work as described in the product. To find the official developer of this product, please refer to the MQL5 website.

For detailed reviews and trading results of this product, please visit [forexroboteasy.com/forex-robot-review/royal-scalping-indicator-m4-review-high-quality-trading-signals/](https://forexroboteasy.com/forex-robot-review/royal-scalping-indicator-m4-review-high-quality-trading-signals/)
