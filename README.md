# Interest Rate Swaption Product and Valuation Practical Guide

An interest rate swaption or interest rate European swaption is an OTC option that grants its owner the right but not the obligation to enter an underlying interest rate swap. There are two types of swaptions: a payer swaption and a receiver swaption.
An payer swaption is also called a right-to-pay swaption that allows its holder to exercise into a swap where the holder pays fixed rates and receives floating rates, while a receiver swaption is also called right-to-receive swaption that allows its holders to exercise into a swap where the holder receives fixed rates and pays floating rates.
Swaptions provide clients with a guarantee that the fixed rate of interest they will pay at some of future time will not exceed certain level. This presentation gives an overview of swaption product and valuation. 
An interest rate swaption or interest rate European swaption is an OTC option that grants its owner the right but not the obligation to enter an underlying interest rate swap. There are two types of swaptions: a payer swaption and a receiver swaption. A payer swaption is also called a right-to-pay swaption that allows its holder to exercise into a swap where the holder pays fixed rates and receives floating rates. A receiver swaption is also called right-to-receive swaption that allows its holders to exercise into a swap where the holder receives fixed rates and pays floating rates. Swaptions provide clients with a guarantee that the fixed rate of interest they will pay at some of future time will not exceed certain level.
Market participants use swaptions to manage interest rate risk arising from their business. A firm might buy a payer swaption if it wants protection from rising interest rates. A corporation holding a mortgage portfolio might buy a receiver swaption to protect against decreasing interest rates that might lead to mortgage prepayment. A company believing that interest rates will not increase much might sell a payer swaption and earns the premium. An institution believing that interest rates will not decrease much might sell a receiver swaption and earns the premium.

	Keywords
Swaption, interest rate swap, payer swaption, receiver swaption, financial product, valuation model.

	Swaption Introduction
	An interest rate swaption or interest rate European swaption is an OTC option that grants its owner the right but not the obligation to enter an underlying interest rate swap. 
	There are two types of swaptions: a payer swaption and a receiver swaption. 
	A payer swaption is also called a right-to-pay swaption that allows its holder to exercise into a swap where the holder pays fixed rates and receives floating rates
	A receiver swaption is also called right-to-receive swaption that allows its holders to exercise into a swap where the holder receives fixed rates and pays floating rates.
	Swaptions provide clients with a guarantee that the fixed rate of interest they will pay at some of future time will not exceed certain level.

	Use of Swaption
	Market participants use swaptions to manage interest rate risk arising from their business.
	A firm might buy a payer swaption if it wants protection from rising interest rates.
	A corporation holding a mortgage portfolio might buy a receiver swaption to protect against decreasing interest rates that might lead to mortgage prepayment.
	A company believing that interest rates will not increase much might sell a payer swaption and earns the premium.
	An institution believing that interest rates will not decrease much might sell a receiver swaption and earns the premium.

	Swaption Payoff
	For a payer swaption, the payoff at payment date T is given by
〖Payff〗_payer=max⁡(0,NA(S_T-S_0)		(1)
where 
N- the notional;
A – the annuity or forward basis point value
S_0 – the fixed rate or contract swap rate at inception
S_T – the swap rate at time T.
	From a receiver swaption, , the payoff at payment date T is given by
〖Payff〗_payer=max⁡(0,NA(S_0-S_T)		(2)

	Valuation
	The present value of a payer swaption is given by
 〖PV〗_payer (t)=NA[SΦ(d_1 )-KΦ(d_2)] 			(1)                          
where
	t   –  valuation date
	N  – notational principal amount
A=∑_(i=1)^n▒〖τ_i D_i 〗 – annuity factor or forward basis point value
S=[D_1-D_n ]⁄A  - forward swap rate
  -  the cumulative standard normal distribution function
	i  –  ith cash flow (swaplet) of the underlying swap from 1 to n
	τ_i=τ(T_(i-1),T_i) – the accrual period ( , ) of the ith cash flow.
	D_i=D(t,T_i)  –  the discount factor
	The present value of a receiver swaption can be expressed as

 〖PV〗_payer (t)=NA[KΦ(〖-d〗_2 )-SΦ(〖-d〗_1 )] 			(2)      
                    
where all notations are the same as (1)

	Practical notes
	A swaption contract contains terms and conditions of the swaption and the underlying swap. For example, it specifies two maturities: swaption maturity and underlying swap maturity.
	The valuation model for pricing a swaption is Black formula that assumes the underlying swap rate follows a log-normal process.
	First, one needs to generate the cash flows of the underlying swap. The generation is based on the start time, end time and payment frequency of each leg, plus calendar (holidays), business convention (e.g., modified following, following, etc.) and whether sticky month end.
	The accrual period is calculated according to the start date and end date of a cash flow plus day count convention 
	Any compounded interest zero rate curves can be used to compute discount factor, of course the formulas will be slightly different. The most common used one is continuously compounded zero rates.
	The other key for accurately pricing an outstanding swaption is to construct an arbitrage-free volatility surface. Unlike a cap/floor volatility surface that is 3 dimensional (maturity – strike – volatility), a swaption volatility surface is 4 dimensional (swaption maturity – underlying swap tenor – strike – volatility).

	A Real World Example
Swaption Specification	Underlying Swap Specification
Buy Sell	Buy	Leg 1 Specification	Leg 2 Specification
Pay Receive	Ray	Currency	USD	Currency	USD
Notification Lag	2	Day Count	dc30360	Day Count	dcAct360
Settlement	Cash	Leg Type	Fixed	Leg Type	Float
Exercise Type	Call	Notional	25000000	Notional	25000000
Notification Date	4/30/2020	Pay Receive	Pay	Pay Receive	Receive
Settlement Date	5/5/2020	Payment Freq	6	Payment Freq	3
Forward Premium Amount	3375000	Start Date	5/5/2020	Start Date	5/5/2020
Premium Pay Receive	Pay	End Date	5/5/2030	End Date	5/5/2030
Forward Premium Date	5/5/2020	Fixed Rate	0.02855	Spread	0
				Index Specification
				Type	LIBOR
				Tenor	3M
				Day Count	dcAct360


Reference:
https://finpricing.com/knowledge.html

