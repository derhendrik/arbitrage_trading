# Arbitrage Trading with Floyd-Warshall Algorithm

This repository contains an implementation of the Floyd-Warshall
Algorithm ([Wikipedia](https://en.wikipedia.org/wiki/Floyd%E2%80%93Warshall_algorithm)) to identify arbitrage
opportunities on foreign exchange markets.

Given a directed graph where nodes represent currencies and arc weights
represent exchange rates between two currencies, the goal is to identify cycles (a trading sequence) that yield a net profit.

Given a sequence of arcs that determine a cycle $C$, it has to hold that $\Pi_{c \in C} \, w_c > 1$ where $w_c$ is the arc weight of arc $c$.

Using the natural log of arc weights, the stated condition can be reformulated as $\Sum_{c \in C} \, -ln(w_c) < 0 $.
