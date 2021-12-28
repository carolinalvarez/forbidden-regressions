# Computational Statistics final project | University of Bonn | Summersemester 2021 

This project explores the performance of some of the ML toolkit resources in the field of instrumental variables (IV). The first stage of a 2SLS method is a prediction problem, in the sense that one aims to predict the endogenous variable  through an exogenous instrument (and some exogenous covariates) in order to plug in fitted values into a second stage to successfully recover the model estimates of interest. Here, the prediction ability of ML methods may sound appealing, given that  better first stage predictions may help to produce more precise second-stage estimates. However, the extent to which ML algorithms actually outperform OLS first stage prediction and thus second stage estimation is a field with very few academic exploration yet.

Here, I partially replicate the research conducted by [Lennon et al. (2021)](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=EbWudV0AAAAJ&alert_preview_top_rm=2&citation_for_view=EbWudV0AAAAJ:ufrVoPGSRksC) and extend it to analyze whether their results are sensitive to the initial data generation process (DGP) specification.  I conducted the study for two specific ML algorithms: random forest and boosting. The simulation study is successfull in replicating the low complexity scenario of Lennon et al (2021) and the variations on their initial DGP suggest that ML methods do generate biased results in a second stage estimation, but the extent of the bias and the relative performance of each method vary according to the DGP set-up.

In a second part, I apply the methods to the [Angrist and Evans (1998)](https://www.jstor.org/stable/116844) Census Data, in order to analyze the performance of the ML algorithms (here random forest, boosted trees and logistic regression) when compared to 2SLS estimations of the effect of childbearing on women labor supply. The results show that, using the IV estimate as a benchmark, nonlinear methods yield biased results, where random forest comes close to the naive OLS estimation while boosting and logit clearly underestimate the coefficients.

# References <a class="anchor" id="ref"></a>

* **Angrist, J., & Evans, W. (1998)**. *[Children and Their Parents' Labor Supply: Evidence from Exogenous Variation in Family Size](https://www.jstor.org/stable/116844)*, 88(3), The American Economic Review.

* **Angrist, J., & Frandsen, B. (2019)**. *[Machine Labor](https://www.nber.org/papers/w26584)*, National Bureau of Economic Research, Working Paper 26584.

* **Angrist, J., & Pischke, J. (2009)**. *[Mostly Harmeless Econometrics: An Empiricist´s Companion](https://www.mostlyharmlesseconometrics.com/)*, Princeton Univeristy Press.

* **Chen, J., Chen, D., & Lewis, G. (2020)**. *[Mostly Harmless Machine Learning: Learning Optimal Instruments in Linear IV Models](https://arxiv.org/abs/2011.06158), 	arXiv:2011.06158.

* **James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013)** *[An Introduction to Statistical Learning](https://link.springer.com/book/10.1007/978-1-4614-7138-7), Springer Texts in Statistics, volume 103.

* **Lennon, C., Rubin, E., & Waddell, G. (2021).** *[What can we machine learn (too much of) in 2SLS?
Insights from a bias decomposition and simulation](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=EbWudV0AAAAJ&alert_preview_top_rm=2&citation_for_view=EbWudV0AAAAJ:ufrVoPGSRksC)*, Working Paper.

* **Mullainathan, S., & Spiess, J. (2017)**. *[Machine Learning: An Applied Econometric Approach](https://www.aeaweb.org/articles?id=10.1257/jep.31.2.87)*, 31(2), Journal of Economic Perspectives.

* **Varian, H. (2014)**. *[Big Data: New Tricks for Econometrics](https://www.aeaweb.org/articles?id=10.1257/jep.28.2.3)*, 28(2), Journal of Economic Perspectives.
