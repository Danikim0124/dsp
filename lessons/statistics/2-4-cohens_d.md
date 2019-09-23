[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> 
Using the variable totalwgt_lb, investigate whether ﬁrst babies are lighter or heavier than others. Compute Cohen’s d to quantify the diﬀerence between the groups. How does it compare to the diﬀerence in pregnancy length?

import math

import os

import thinkstats2

import nsfg


preg = nsfg.ReadFemPreg()

live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]

others = live[live.birthord != 1]


CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

CohenEffectSize(firsts.prglngth, others.prglngth)


Cohen's d for first babies vs. others is about -0.089. This means first babies are about 0.089 std. lighter than others 

Cohen's d in pregnancy length is about 0.03. This means that first babies have about 0.03 std. longer pregnancy length than others.

