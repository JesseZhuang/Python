## Precision

What percentage of positive identifications was correct?

$precision = \frac{TP}{TP + FP}$

example: analyze tumors, predict 2 of 100 positive, presicion is 0.5.

Confusion matrix:

|||
|-|-|
|True Positives (TPs): 1|False Positives (FPs): 1|
|False Negatives (FNs): 8|True Negatives (TNs): 90|

## Recall

What percentage of actual positives was identified correctly?

$Recall = \frac{TP}{TP + FN} = \frac{1}{1 + 8} = 0.11$

With the example above, the model predicts 2 of 100 positive. Recall is 0.11.

## Prevision and Recall

Unfortunately, precision and recall are often in tension. That is, improving precision typically reduces recall and vice versa.



## Classification: ROC Curve and AUC

An ROC curve (receiver operating characteristic curve) is a graph showing the performance of a classification model at all classification thresholds.
