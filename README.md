# SimpleForexMACD_Strategy_Bot

MagicNumber - This is a unique identifier for the EA, if the EA is run on different charts just make the MagicNumbers different to avoid interference

HigherTimeFrame - Self explanatory I guess

MinBarsCount - This is the minimum number of bars on the MACD indicator to validate a swing high/low any thing less is not considered valid

LossOffsetFactor - The SL is calculated based on the candle with the swing high or low, the extremes of the candle gives the entry price and SL. However SL can be modified to be LossOffsetFactor(entry-SL)

RiskReward - TP is set based on a fixed RR

Modify2BE_AtRR - This should only be considered if Set2BE is true, it pretty much modifies to BE when a specified RR is reached

RiskPercent - Every trade risks a fixed percentage of the account, the percentage is specified here.

RiskCorrectionFactor - This is very important, it differs from broker to broker and sometimes from pair to pair for the same broker. It should be adjusted to make sure that the specified risk is being observed. Use strategy tester to see which value you need to use. The values I have used are 100, 10, 1, 0.1, 0.001. Just play around with those. A mistake here can tenfold your risk.

lot_digits - This is usually fine at 2, however some brokers don't allow micro and mini lots in the strategy tester on some pairs. In cases like that, this should be changed to zero.

Modify3 - This is a trade management function that leads TP and trails SL. I don't usually use it though but it's worth a shot.

Set2BE - This is just asking whether you want to set your trades to B.E at a certain RR given by Modify2BE_AtRR 

CloseAfterHours - This is asking if open trades should be closed at StopHour

ExpirationBars - This is asking the number of bars after which unexecuted pending orders should be expired

fast_ema,slow_ema,signal_period, SignalMethod,AppliedPrice - These are MACD settings, they can be changed as necessary

StartHour, StopHour - This is the time range in which the EA should trade, this is based on your broker time not your time.






