# Put and Call Payoff and Greeks

This all start with Black and Scholes (BS), which is a mathematical formula that is used to determine the price of a European Call (or Put) on a financial instrument. The model assumes that asset price movement follow a geometric Brownian motion with constant drift and volatility, the random increment or price change will be normally distributed with infinitesimal variance.

Assuming that the asset price S follow the following process:

![equation](https://latex.codecogs.com/svg.latex?dS=\mu{S}dt+\sigma{S}dW)

where ![equation](https://latex.codecogs.com/svg.latex?\mu) and ![equation](https://latex.codecogs.com/svg.latex?\sigma) are constant. t stands for time and ![equation](https://latex.codecogs.com/svg.latex?W) is a Wiener process (process of mean change of zero and variance equal to ![equation](https://latex.codecogs.com/svg.latex?\Delta{t})) 

From this it is possible to derive the Black-Sholes equation.

## Greeks

The Greeks are the model outputs from Black-Scholes, they provide information about the sensitivity of outputs of the model to change in the inputs into the model.

Delta: Measures the rate of change in the option value with respect to changes in the underlying asset's price (the first derivative of the option price with respect to the underlying price). It loosely equal the probability that the option finishes in-the-money. Delta for a Call ranges from o to 1, and from -1 to 0 for a put.

Gamma: Measures the rate of change of the option delta with respect to the change in the underlying asset price (the second derivative of the option price with respect to the underlying price). Even if the underlying asset price remains unchanged, the option delta for an in-the-money option increases as expiration nears, the opposite is true for an out-of-the-money option. 
The gamma of an option indicates how the delta of an option will change for a one-point move in the underlying asset. The gamma shows the option delta's sensitivity to market price changes. Gamma is important for maintaining a delta neutral position.

Vega: Measures the sensitivity of the option to changes in implied volatility. It equals the first derivative of the option price with respect to the volatility of the underlying asset. Vega is typically expressed as the amount of money per underlying share that the option's value will gain or lose as volatility rises or falls by 1%. Vega is most sensitive when the option is at-the-money and tapers off either side as the market trades above/below strike. Straddle is an example of strategy vega sensitive.

Theta: Measures how fast the premium of an option decays with time or how much value an option's price will diminish per day. It is not possible to hedge the passage of time. The nearer the expiration date, the higher the theta. Option trading strategies that are particularly theta sensitive include Calendea Spreads, where the trader maintains a net positive theta buying longer dated options and selling shorter dated ones, profiting when the underlying stock remains within a tight range.

Rho: Measures the sensitivity of a stock option's price to a change in interest rates, typically changes in interest rate over short time period have very little effect on options where the underlying asset is not rate sensitive (equities instead of bonds for example). Call option rise in value when interest rates hike, the oppposite is true for puts. Rho increases as time to expiration becomes longer.
