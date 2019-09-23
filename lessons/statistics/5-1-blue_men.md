[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.
In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.

About 34% of U.S. male population can join Blue Man Group (height between 5’10” and 6’1”)

```python
mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)

# How many people are betweene 5'10" and 6'1"?

## 5'10"
low = dist.cdf(177.8)
print(low)

## 6'1"
high = dist.cdf(185.42)
print(high)

print(high - low)
```
