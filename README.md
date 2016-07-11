# skillmack-matlab
Nonparametric Two-way ANOVA Used For Block Designs with Missing Observations

The Skillings-Mack statistical test is a nonparametric ANOVA-like test used for incomplete block designs, when the number of observations in each treatment/block pair is one or zero. The test is equivalent to the Friedman test when no observations are missing. 

Syntax: 
[p stats] = skillmack(response, treatments, blocks) 
[p stats] = skillmack(M) % Where columns are treatments and rows are blocks 

Example: (see anova1 function for explanation of hogg data) 
load hogg 
friedman(hogg,1) 
skillmack(hogg) 
hogg(5) = NaN; 
skillmack(hogg) 

Skillings, J. H., & Mack, G. A. (1981). On the Use of a Friedman-Type Statistic in Balanced and Unbalanced Block Designs. Technometrics, 23(2), 171-177.
See also: Hollander, M., & Wolfe, D. A. (1999). Nonparametric statistical methods (2nd ed.). New York: Wiley.
