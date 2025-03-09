# SDE-Research-Summer2024
This repository is the summary of weekly report of work of SDE research on Summer 2024. The main task is to find the optimal SDE such that it accurately reasons the factors affecting a selected set of stock and derivatives price and describe it accurately with efficient numerical method implemented.

Participants: Jiahua Song, Fangshuo Liu

# Dynamical Update (Tentative):
https://docs.google.com/document/d/1UF_Txlt13-l1EuiwOLOv_tkfk4BbjNMEA24hERhPO18/edit

# Structure of Work:
[Yifan, Fangshuo]
I (Data):
1.	Stocks & Derivatives (e.g. Stock selection factor; Momentum; Bollinger) (Tech, with appropriate volatility)
2.	Hyperparameters (Fed interest rate, vol(x,y,z,...): XxYxZ -> R, p(w1(t), w2(t,x), …))

[Yisheng, Jiahua]
II (Theory):
1.	dX_t = b(X_t, t)dt + \sigma(X_t, t)dW_t, (X_t stocks’ price)
2.	[Paper] Find an “optimal” SDE such that it satisfies the historical data gained in I. 
a.	Heston, VGSA, … (dXt = …, dVol(x,y, z) = …) sensitivity test on hyperparameters, Merton-Jump model
b.	For Black Swan event, set a parameter “impact” (0, 1), maybe use t-1 data to estimate the “impact” on t.
c.	Optimal control theory
3.	[Paper] Optimization Expectation (f(t) = Return => E(f) => PDE => max E(f) subject to g(t)\ leq 1, dXt = ….) HJB

[Jiahua 1, Yifan 1, Fangshuo 2, Yisheng 2]
III (Numerical Implementation):
1.	[Paper] Algorithm (Taylor-Itô => consistency, dX_t = b(X_t, t)dt + \sigma(X_t, t)dW_t => stability region, Lax-Equivalence => convergent) 
2.	Implementation (“Correct”) (python => auto) 

Target: 
1.	Best SDE fitting the data
2.	Code work for realization
Output: Paper and Project(GitHub)
Advisors: Shanyin Tong, Mikhail Smirnov, Ali Hirsa
