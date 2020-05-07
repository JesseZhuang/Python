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

## Stratum

Ref:
- https://www.statisticshowto.com/stratum/
- https://www.statisticshowto.com/stratified-random-sample/

Stratum in geology or biology refers to layers, as in a layer of rock or layer of skin. A stratum in statistics isn’t much different — you can think of it as where your target population is divided into non-overlapping layers, subgroups, or categories. For example, strata could define the socioeconomic statuses of a population:

1: Lowest 25 percent of wage earners.
2: Middle 50 percent of wage earners.
3: Highest 25 percent of wage earners.

“Stratum” refers to a single subgroup or category, while “Strata” can mean several, or all, groups.

Strata do not need to be in layers. They can be categories that contain different geographical areas, different backgrounds, different races or other categorical definitions. The main point is that each stratum is completely distinct and that the strata do not overlap.

**How to Get a Stratified Random Sample**

Sample question: You work for a small company of 1,000 people and want to find out how they are saving for retirement. Use stratified random sampling to obtain your sample.

Step 1: Decide how you want to stratify (divide up) your population. For example, people in their twenties might have different saving strategies than people in their fifties.

Step 2: Make a table representing your strata. The following table shows age groups and how many people in the population are in that strata:

Age|Total Number of People in Strata
-|-
20-29|	160
30-39|	220
40-49|	240
50-59|	200
60+|	180


Step 3: Decide on your sample size. For this example, we’ll assume your sample size is 50.

Step 4: Use the stratified sample formula (Sample size of the strata = size of entire sample / population size * layer size) to calculate the proportion of people from each group:

Age|Number of People in Strata|Number of People in Sample
-|-|-
20-29|160|50/1000 * 160 = 8
30-39|220|50/1000 * 220 = 11
40-49|240|50/1000 * 240 = 12
50-59|200|50/1000 * 200 = 10
60+|180|50/1000 * 180 = 9

Note that all of the individual results from the stratum add up to your sample size of 50: 8 + 11 + 12 + 10 + 9 = 50

Step 5: Perform random sampling (i.e. simple random sampling) in each stratum to select your survey participants.

That’s how to get a stratified random sample!

Tip: Each element in your population should only fit into one stratum. In other words, one person cannot be in more than one group.
