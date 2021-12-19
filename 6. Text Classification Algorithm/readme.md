
# Text Classification Algorithms

Classification algorithms can be characterized into the fol‐
lowing categories:

* Binary Classification


## Binary classification
This is actually a special case of multiclass classification where an observation can
have any one of two values (binary). For example, a given email can be marked as
spam or not spam. But each observation will have only one label.

## Multiclass classification
In this type of classification algorithm, each observation is associated with one
label.

## Multilabel classification
In this type of classification algorithm each observation can be assigned to multi‐
ple labels.


## Precision
This metric tells us what proportion of predicted positives is actually positive, or how
accurate our model is at predicting the positive class.

## Recall
This metric tells us what proportion of real positive values is actually identified by
our model. A high recall means that our model is able to capture most of the positive
classifications in reality.

## Treating Class Imbalance
* Upsampling
Upsampling techniques refer to methods used to artificially increase the number of observa‐
tions of the minority class. These techniques can vary from simply adding multiple copies to generating new observations using a method like SMOTE

* Downsampling
Downsampling techniques refer to methods that are used to reduce the number of observations of the majority class

* SMOTE
Using this method we don’t just create copies of the same observation but
instead synthetically generate new observations that are similar to the minority class.
