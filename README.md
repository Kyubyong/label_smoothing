# Noisy Labels and Label Smoothing

When we apply the cross-entropy loss to a classification task, we're expecting true labels to have 1, while the others 0. In other words, we have no doubts that the true labels are true, and the others are not. Is that always true? Maybe not. Many manual annotations are the results of multiple participants. They might have different criteria. They might make some mistakes. They are human, after all. As a result, the ground truth labels we have had perfect beliefs on are possible wrong.

One possibile solution to this is to relax our confidence on the labels. For instance, we can slighly lower the loss target values from 1 to, say, 0.9. And naturally we increase the target value of 0 for the others slightly as such. This idea is called label smoothing. Consult [this](https://arxiv.org/abs/1512.00567) for more information.

In this short project, I examine the effects of label smoothing when there're some noise. Concretly, I'd like to see if label smoothing is effective in a binary classification/labeling task where both labels are noisy or only one label is noisy.
