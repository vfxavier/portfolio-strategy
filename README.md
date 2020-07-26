# Data Science - Portfolio Strategy

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/vfxavier/portfolio-strategy/master)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/vfxavier/portfolio-strategy/)

## Real Estate Portfolio Optimization

In this repository we explore fictious properties sales listings   throughout a semester with the objective of finding the main drivers for it's prices and liquidity. Thereon we build optimal portfolios given different risk thresholds. The badges above allow readers to reproduce this entire analysis using binder environments or to copy notebooks to a private Google Colaboratory repository. 

## Action Plan

#### Pricing:
Our first steps will be exploring and cleaning the data (EDA) followed by a baseline pricing model using **multiple linear regression**. We will then train gradient boosted decision trees using XGBoost and evaluate the benefits of the added complexity. 

#### Liquidity:
Using the same techniques above we will try to understand the relationship between a given property attributes, it's price and the expected time for it's sale. We will also use the same variables to predict the probability of a property being sold, representing the risk of that investment.

#### Portfolio Optimization:
The optimization will consist in finding the expected value of each individual investment given certain constraints. This will be achieved by maximizing the revenue by time unit, as seen below.

<img src="https://render.githubusercontent.com/render/math?math=E(x) = \sum{\frac{S_i - P_i}{T_i} \times P(x)}">

(Sale - Purchase) / (Time to Sell) * Sale Probability

#### Future Work:
Explore how concepts like *Markowitz's Efficient Frontier* and *Sharpe Ratio* can help in the process of building such portfolios.
To do so, we will probably need to evaluate the price variance of a given set of properties, which could be accomplished by:
1. Clustering similar properties and evaluating the intra-cluster price variance;
1. Use of bayesian methods to estimate the confidence of a given prediction.

## Assumptions

## Proposed Questions

## Conclusion and Business Impact

## Premissas:
1. Pagar exatamente o valor na coluna value
1. A reforma traz o apartamento para o melhor estado de conservação `(interior_quality=3)`
1. Capital disponível para composição do portfólio é de R$150 Mi

## Roteiro proposto:
1. **Liquidez x Preço**
    1. Criar modelo estimando preço e tempo até venda
        1. Variáveis mais importantes
        1. Como usar a informação de tempo dos apartamentos que ainda não foram vendidos?
    1. Qual o efeito da liquidez no preço e vice-versa?
    1. Quantos dias a menos um apartamento levaria para vender se fosse 10% mais barato?


1. **Alocação de portoflio**
    1. Criar modelo que maximize a receita por unidade de tempo 
        1. (preço de venda - preço de compra)/(tempo esperado no mercado)


1. **Efeito do estado de conservação**
    1. Como ela influencia no preço e na liquidez?
    1. Como isolar esse efeito?

## Entregável deve conter:
1. Lógica utilizada
1. Suposições feitas
1. Repercussão para o negócio
