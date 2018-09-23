[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

# Question 5-1:

Exercise: In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.

In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

# Solution 5-1:

import scipy.stats

mu = 178

sigma = 7.7

dist = scipy.stats.norm(loc=mu, scale=sigma)

type(dist)


dist.mean(), dist.std()


dist.cdf(mu-sigma)

low = dist.cdf(177.8)    # 5'10"

high = dist.cdf(185.4)   # 6'1"

low, high, high-low


__83% of males are equal to or under 6'1" and 48% are equal to or under 5'10". 83-48 = 34. 34% of males are allowed to apply for the blue man group.__
