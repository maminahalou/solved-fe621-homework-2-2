Download Link: https://assignmentchef.com/product/solved-fe621-homework-2-2
<br>
<strong>Problem 1. The Binomial Tree.</strong>

<ul>

 <li>Construct code to calculate option values using <em>an additive binomial tree</em>. For this part you need four versions: European and American as well as Call and Put. You <em>may </em>use the same tree construction (and function) for all options.</li>

 <li>Download Option prices (you can use the Bloomberg Terminal, Yahoo! Finance, etc.) for an equity, for 3 different maturities (1 month, 2 months, and 3 months) and 20 strike prices close to the value at the money. If 3 months does not exist use next one available. Please download the data DURING THE TRADING DAY (9:00am to 4:30pm ET). Otherwise your values will be way off. Do not forget to download the value of the underlying. For each strike price in the data, use the implied vol values in Homework 1 (see Problem 1c) and the current short-term interest rate (today the Feds Fund rate is <em>r </em>= 0<em>.</em>75%). Calculate the option price (European Calls and Puts) using the binomial tree, and compare the results with the Black–Scholes price. Use at least 200 steps in your tree construction. Treat the options as American as well and plot these values side by side with the European and Black Scholes values. When you create the plot do not forget to plot the bid-ask values as well. If you downloaded DATA 2 for last assignment you can use that as your data set.</li>

 <li>Comment of the table in the previous part.</li>

 <li>Consider <em>N </em>∈{10<em>,</em>20<em>,</em>30<em>,</em>40<em>,</em>50<em>,</em>100<em>,</em>150<em>,</em>200<em>,</em>250<em>,</em>300<em>,</em>350<em>,</em>400}. Compute and plot the absolute error for the European Put <em>ε<sub>N </sub></em>for as a function of</li>

</ul>

<em>N </em>∈N<sup>∗ </sup>the number of steps in the tree:

<em>,</em>

where <em>C<sup>BSM</sup></em>(<em>S</em><sub>0</sub><em>,K,T,r</em>;<em>σ</em>) and <em>C<sub>N</sub><sup>BinomTree</sup></em>(<em>S</em><sub>0</sub><em>,K,T,r</em>;<em>σ</em>) are the Black– Scholes–Merton price and the price calculated using a binomial tree with <em>N </em>steps, respectively. What do you observe?

Using the binomial tree for American Calls and Puts, calculate the implied volatility corresponding to the data you have downloaded in part (b). You will need to use the bisection or Newton/secant method of finding roots with the respective binomial trees. Compare these values of the implied volatility with the volatilities calculated using the usual Black Scholes formula (as in Homework 1, Problem 1c). Write detailed observations.

<strong>Problem 2 The Trinomial Tree.</strong>

<ul>

 <li>Implement a trinomial tree to price European, American Call and Put options. See Chapter 3 in [1].</li>

 <li>Consider <em>S</em><sub>0 </sub>= 100<em>,K </em>= 100, <em>T </em>= 1 year, <em>σ </em>= 25%<em>,r </em>= 6%<em>,δ </em>= 0<em>.</em> Repeat the methods in problem 1 b) to d) with these parameters. Use at least <em>N </em>= 200 time steps and you do not need to download data. Make sure√</li>

</ul>

that convergence condition holds, i.e. ∆<em>x </em>≥ <em>σ </em>3∆<em>t </em>(see Section 3.5 in [1]). Create a table containing all results and comment

<strong>Problem 3 Pricing Exotic Options. </strong>We will use here a synthetic example to illustrate the power of the tree models. Please read Section 2.10 in [1] and Sections 1 and 5.1 in [2] (available <a href="https://www.math.kth.se/matstat/seminarier/reports/K-exjobb09/090601a.pdf">here</a><a href="https://www.math.kth.se/matstat/seminarier/reports/K-exjobb09/090601a.pdf">)</a>, and solve the following problems.

<ol>

 <li>Construct a binomial tree to calculate the price of an European Up-and-Out call option. Use <em>S</em><sub>0 </sub>= 10, strike <em>K </em>= 10, maturity <em>T </em>= 0<em>.</em>3, volatility <em>σ </em>= 0<em>.</em>2, short rate <em>r </em>= 0<em>.</em>01, dividends <em>δ </em>= 0, and barrier <em>H </em>= 11. Use as many steps in your tree as you think are necessary. Read the algorithm in the book [1] and try and figure out how to modify the code there to work with the new option.</li>

 <li>For the European Up-and-Out Call option explicit formulas exist. For example, implement the formula (5.2) from [2] and compare your results with part (a). Use the same parameters as before. Are your results matching?</li>

 <li>Price an European Up-and-In call option, using the same parameters as before. Two methods can be employed: the analytical solution in (5.1) or the In-Out parity. Use both methods in order to verify your results.</li>

 <li>Calculate the price of an AMERICAN Up and In Put option</li>

</ol>

<strong>Problem 4 Finite difference methods.</strong>

<ul>

 <li>Implement the Explicit Finite Difference method to price both European Call and Put options. See Chapter 3 in [1].</li>

 <li>Implement the Implicit Finite Difference method to price European Call and Put options.</li>

 <li>Implement the Crank-Nicolson Finite Difference method and price both European Call and Put options.</li>

 <li>For both the Explicit and Implicit Finite Difference schemes estimate the numbers ∆<em>t</em>, ∆<em>x </em>as well as the total number <em>N<sub>j </sub></em>of points on the space grid <em>x </em>to obtain a desired error of <em>ε </em>= 0<em>.</em> <em>Hint. </em>You need to this part in a theoretical way. Please use the convergence order as the actual error of the estimate.</li>

 <li>Consider <em>S</em><sub>0 </sub>= 100<em>,K </em>= 100, <em>T </em>= 1 year, <em>σ </em>= 25%<em>,r </em>= 6%<em>,δ </em>= 0<em>.</em></li>

</ul>

Calculate and report the price for European Call and Put using explicit, implicit FD and Crank-Nicolson methods and the number of steps that you calculated in the previous point (part d).

<ul>

 <li>Repeat part (d) of this problem but this time get the empirical number of iterations. Specifically, obtain the Black Scholes price for the data in (e), then do an iterative procedure to figure out the ∆<em>x</em>, ∆<em>t</em>, <em>N</em>, and <em>N<sub>j </sub></em>to obtain an accuracy of <em>ε </em>= 0<em>.</em> Put the results of the 3 methods (EFD, IFD, CNFD) side by side in a table and write your observations.</li>

</ul>

Implement the Rannacher modification [3], that is, replace the first time step of the Crank-Nicolson method with either two half steps or four quarter steps of implicit method. The modification ensures second order convergence for rough payoff functions.

<strong>Bonus Problem A multinomial recombining tree for general Stochastic Volatility models. </strong>We consider here an interesting method of option pricing under general assumptions, involving a multinomial recombining tree and particle filtering techniques. Please read the paper [4], and pay special attention to sections 3 and 4.1, 4.2.

<ul>

 <li>Using synthetic parameters, i.e., chosen by you, estimate the probability distribution for the volatility process <em>Y<sub>t </sub></em>at discrete time points <em>t</em><sub>1</sub><em>,t</em><sub>2</sub><em>,…,t<sub>n</sub></em>. To this end, implement the particle filter described in Section 3 of [4]. You should store from this step the particles {<em>Y</em><sup>¯</sup><sub>1</sub><em>,Y</em><sup>¯</sup><sub>2</sub><em>,…,Y</em><sup>¯</sup><em><sub>n</sub></em>} together with their corresponding probabilities {<em>p</em><sub>1</sub><em>,p</em><sub>2</sub><em>,…,p<sub>n</sub></em>}.</li>

 <li>Construct the successors in the multinomial tree with synthetic parameters, see Section 4.1. Please note that two separate cases were analyzed.</li>

 <li>You built in part (b) the one period model. Implement now the multi-period model described in Section 4.2. Price for illustrative purposes the European Call option and try to replicate the results in Section 6 of the paper.</li>

 <li>Build a multinomial tree as in [4] to price an American Put Option. Compare your results with Problem 4(a).</li>

 <li>The most important limitation here is that the two Brownian Motions <em>W<sub>t </sub></em>and <em>Z<sub>t </sub></em>in equation (1.1) are assumed independent, i.e.</li>

</ul>

E[W. <em><sub>t</sub></em>Z.<em><sub>t</sub></em>] = 0<em>.</em>

√                      √

To circumvent this, let <em>σ</em>(<em>y</em>) =         <em>y</em>, <em>ψ</em>(<em>y</em>) = <em>γ            y</em>, and E[W. <em><sub>t</sub></em>Z.<em><sub>t</sub></em>] = <em>ρ </em>in (1.1), i.e., the Heston Model, and consider the transformation

<em>, </em>where

Apply Ito’s Lemma on <em>X<sub>t </sub></em>and show that X. <em><sub>t </sub></em>can be written as X. <em><sub>t </sub></em>= <em>µ<sub>X</sub></em>(<em>t</em>)t. + <em>σ<sub>X</sub></em>(<em>t</em>)B. <em><sub>t</sub></em>, where <em>B<sub>t </sub></em>is uncorrelated with <em>W<sub>t</sub></em>, and <em>µ<sub>X</sub>,σ<sub>X </sub></em>are real– valued functions. Build a multinomial tree as in [4] to price an American Put Option. Compare your results with Problem 4(a) and part (d) of this problem.