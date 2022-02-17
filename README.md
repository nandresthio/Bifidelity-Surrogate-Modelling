## Bi-fidelity Surrogate Modelling

This repo contains the code used to run and analyse all experiments of "Bi-fidelity Surrogate Modelling: Showcasing the need for new test instances" (2022) by Andres-Thio N, Munoz MA, and Smith-Miles K. 

The code implements Kriging[^1][^2] and Co-Kriging[^3][^4] as surrogate models. That is, the implementation
generates a sample of a bi-fidelity function and trains the surrogate model, without the added functionality
of choosing further samples. Multiple literature test instances are implemented here[^6][^7][^8][^9][^10][^11][^12][^13][^14][^15][^16], as well as a novel instance creation procedure which adds a disturbance to a high-fidelity function to create a low-fidelity function. In this implementation functions from the COCO test suite[^17] are used as the high fidelity functions.

All instructions on how to re run all experiments are given in the 'runAllExperiments.bash' file. As given, all experiments and analysis can be run sequentially by simply running the script, although this is not recommended. Instead it is recommmended to use a computer cluster to run the main experiments as indicated in the bash script.

After completing all experiments and analysis, the folder 'data' and its subfolders should contain all of the experimental results and analysis plots. The same folder containing all of the data is given HERE LINK. Note however that the features of the instances created using the COCO suite and disturbances will vary based on the system these experiments are run on, as function instanciation includes randomness. Whilst all random functions are seeded by constants to allow for reproducibility, the random sequences generated by different systems might vary.



[^1]: Krige DG (1951) "A statistical approach to some basic mine valuation problems on the witwatersrand". Journal of the Southern African Institute of Mining and Metallurgy 52(6):119–139.
[^2]: Jones DR (2001) "A taxonomy of global optimization methods based on response surfaces". Journal of global optimization 21(4):345–383.
[^3]: Kennedy MC, O’Hagan A (2000) "Predicting the output from a complex computer code when fast approximations are available". Biometrika 87(1):1–13.
[^4]: Forrester AI, S ́obester A, Keane AJ (2007) "Multi-fidelity optimization via surrogate modelling". Proceedings of the royal society a: mathematical, physical and engineering sciences 463(2088):3251–3269.
[^5]: Toal DJ (2015) "Some considerations regarding the use of multi-fidelity kriging in the construction of surrogate models". Structural and Multidisciplinary Optimization 51(6):1223–1245.
[^6]: Song X, Lv L, Sun W, Zhang J (2019) "A radial basis function-based multi-fidelity surrogate model: exploring correlation between high-fidelity and low-fidelity models". Structural and Multidisciplinary Optimization 60(3):965–981.
[^7]: March A, Willcox K (2012) "Provably convergent multifidelity optimization algorithm not requiring high-fidelity derivatives". AIAA journal 50(5):1079–1089.
[^8]: Rajnarayan D, Haas A, Kroo I (2008) "A multifidelity gradient-free optimization method and application to aerodynamic design". 12th AIAA/ISSMO multidisciplinary analysis and optimization conference, 6020.
[^9]: Liu B, Koziel S, Zhang Q (2016) "A multi-fidelity surrogate-model-assisted evolutionary algorithm for computationally expensive optimization problems". Journal of computational science 12:28–37.
[^10]: Wang H, Jin Y, Doherty J (2017) "A generic test suite for evolutionary multifidelity optimization". IEEE Transactions on Evolutionary Computation 22(6):836–850.
[^11]: Liu H, Ong YS, Cai J, Wang Y (2018b) "Cope with diverse data structures in multi-fidelity modeling: a gaussian process method". Engineering Applications of Artificial Intelligence 67:211–225.
[^12]: Wu Y, Hu J, Zhou Q, Wang S, Jin P (2020) "An active learning multi-fidelity metamodeling method based on the bootstrap estimator". Aerospace Science and Technology 106:106116.
[^13]: Shi M, Lv L, Sun W, Song X (2020) "A multi-fidelity surrogate model based on support vector regression". Structural and Multidisciplinary Optimization 1–13.
[^14]: Dong H, Song B, Wang P, Huang S (2015) "Multi-fidelity information fusion based on prediction of kriging". Structural and Multidisciplinary Optimization 51(6):1267–1280.
[^15]: Xiong S, Qian PZ, Wu CJ (2013) "Sequential design and analysis of high-accuracy and low-accuracy computer codes". Technometrics 55(1):37–46.
[^16]: Park C, Haftka RT, Kim NH (2018) "Low-fidelity scale factor improves bayesian multi-fidelity prediction by reducing bumpiness of discrepancy function". Structural and Multidisciplinary Optimization 58(2):399–414.
[^17]: Hansen N, Auger A, Ros R, Mersmann O, Tuˇsar T, Brockhoff D (2020) "COCO: A platform for comparing continuous optimizers in a black-box setting". Optimization Methods and Software URL http://dx.doi.org/https://doi.org/10.1080/10556788.2020.1808977


