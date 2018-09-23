[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

# 3.1 Question

Something like the class size paradox appears if you survey children and ask how many children are in their family. Families with many children are more likely to appear in your sample, and families with no children have no chance to be in the sample.

Use the NSFG respondent variable numkdhh to construct the actual distribution for the number of children under 18 in the respondents' households.

Now compute the biased distribution we would see if we surveyed the children and asked them how many children under 18 (including themselves) are in their household.

Plot the actual and biased distributions, and compute their means.

# 3.1 Solution


resp = nsfg.ReadFemResp()

pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

thinkplot.Pmf(pmf)

thinkplot.Config(xlabel='Number of children', ylabel='PMF')

biased = BiasPmf(pmf, label='biased')

thinkplot.PrePlot(2)

thinkplot.Pmfs([pmf, biased])

thinkplot.Config(xlabel='Number of children', ylabel='PMF')



pmf.Mean()
biased.Mean()

__The true mean and the biased mean are very different. It is important to look out for potential sources of bias in data sets in order to present an actual picture of what is going on.__
