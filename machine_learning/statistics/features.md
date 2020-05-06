## Jaccard Similarity/Index

Ref:
- https://www.statisticshowto.com/jaccard-index/
- https://en.wikipedia.org/wiki/Jaccard_index

$Jaccard Index = (the number in both sets) / (the number in either set) * 100$

$J(X,Y)=\frac{X \cup Y}{X \cap Y}$

A simple example using set notation: How similar are these two sets?

$A = {0,1,2,5,6}$

$B = {0,2,3,4,5,7,9}$

Solution: J(A,B) = |A∩B| / |A∪B| = |{0,2,5}| / |{0,1,2,3,4,5,6,7,9}| = 3/9 = 0.33.

Notes:

The cardinality of A, denoted |A| is a count of the number of elements in set A. Although it’s customary to leave the answer in decimal form if you’re using set notation, you could multiply by 100 to get a similarity of 33.33%.

Example problem without set notations: Researchers are studying biodiversity in two rain forests. They catalog specimens from six different species, A,B,C,D,E,F. Two species are shared between the two rain forests. What is the Jaccard coefficient?


Solution:

Two species (3 and 5) are shared between both populations. There are 6 unique species in the two populations.

$2/6 = 1/3 = 33.33%.$

Rainforests A and B are 33% similar.

### Jaccard Distance

A similar statistic, the Jaccard distance, is a measure of how dissimilar two sets are. It is the complement of the Jaccard index and can be found by subtracting the Jaccard Index from 100%. For the above example, the Jaccard distance is 1 – 33.33% = 66.67%.

In set notation, subtract from 1 for the Jaccard Distance:

$D(X,Y) = 1 – J(X,Y)$

Note though, that the decimals are usually converted to percentages as these are easier to interpret.

What to do with missing values?

Sometimes data sets will have missing observations, which makes calculating similarity challenging. You have several options for filling in these missing data points:
- Fill in the blank areas with zeros
- Replace the missing values with the median for the set
- Use a k-nearest neighbor or [EM algorithm](https://www.statisticshowto.com/em-algorithm-expectation-maximization/)
