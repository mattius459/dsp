[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)
                                   
# 2-4 Question:
                                   
Exercise 2.4 Using the variable totalwgt_lb, investigate whether first babies
are lighter or heavier than others. Compute Cohen’s d to quantify the
difference between the groups. How does it compare to the difference in
pregnancy length?                               

# 2-4 Solution:
                                   

`firsts_weight = firsts.totalwgt_lb.mean()`

`others_weight = others.totalwgt_lb.mean()`

`def CohenEffectSize(group1, group2):`

  `diff = group1.mean() - group2.mean()
  
  var1 = group1.var()
  
  var2 = group2.var()
  n1, n2 = len(group1), len(group2)
  pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
  d = diff / math.sqrt(pooled_var)
  return d
  `
                                   
                                   
`CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)`                                   

__The effect is is negative, which means that the first group is a little lighter than the others group. This makes sense since the first child pregnancy length is shorter than for later children, giving the baby less time to grow. The effect is quite small as well.__
                                   
                                   
                                   
                                   
                                   
                                   
                                   
                                   
                                   
                                   
