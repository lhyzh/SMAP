# SMAP
This repository contains Julia and Python programs that implement some of the tools described in my book "Stochastic Methods in Asset Pricing" (SMAP), MIT Press 2017 (with some amendments and extensions that are not covered in the book). The Julia code (posted in both .ipynb and .jl formats and tested with v.1.1.0) is more recent, better written, and much faster. Among other things, the program for computing the price and the exercise boundary of American call options in the Black-Scholes-Merton framework (section 18.4 in SMAP) can now be completed in about 14 seconds (11 seconds on two CPU cores -- processor i7-8650U and OS CentOS Linux). From practical point of view, the use of multiple CPU cores is not particularly meaningful, but serves the purpose of illustrating the way parallel computing can be implemented in such a context. The Python version of the same program (single core) completes for about 1 min with 10 iterations and 78 grid points, whereas the Julia version uses 5,000 grid points and 23 iterations (to complete in 14/11 seconds). This approach is very different from the classical Monte Carlo, binomial lattice, or PDE methods.

Some more mundane task, such as storing, analyzing, and uploading market data, in addition to simulating multivariate normal samples for a given covariance matrix, building historams, etc., are also implemented and updated to the most recent Julia release. 

A technical note: The archive 'HistoricalQuotes.tar' must be untarred in the same directory in which the notebook that is using it is located (it assumes the existence of a subdirectory called 'HistoricalQuotes'). This can be done from within the notebook by executing the shell command (note the semicolon)

; tar xvf HistoricalQuotes.tar
