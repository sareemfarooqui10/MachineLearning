Implemented a novel and efficient method using terms-based discriminative information space for robust text classification. Terms in the documents are assigned weights according to the 
discrimination information they provide for one category over the others. These weights also serve to partition the terms into category sets. A linear opinion pool is adopted for combining
the discrimination information provided by each set of terms to yield a feature space (discriminative information space) having dimensions equal to the number of classes. Subsequently, 
a discriminant function is learned to categorize the documents in the feature space.

- A document vector is prepared on the basis of term occurrence and not term frequency to produce more accurate classifiers
- Stopword removal and all preprocessing
- To produce discrimination information for each term, we must first compute the likelihood of it appearing in a category k document which should be greater than its likelihood in
  appearing in other category documents.
- The RR and OR will have their minimum value 1 and the log functions of both should have minimum of 0
- To avoid probability of a term in a document being zero, add-one laplacing is done to avoid division-by-zero error during weight computation.
- Although weights of every English word is computed, the terms are partitioned into relevant and irrelevant terms, later are removed from classification model. The terms are found
  relevant if the discrimination value is higher than the value of the threshold.
- On the basis of set of terms whose occurrence chances in category k is greater than that in category not k and the set of terms whose occurrence chances are greater in category not
  k than occurrence chances in category k, we computed two scores of each document relative to each category, score with category k and score with category not k. Using these scores, we
  built term partition space.
- Once we have a graph plot of the feature space, we can easily compute the slope and bias parameter. We also assign a document’s category using the linear discriminant function.

***********Conclusion***********
Relative Risk performs relatively better among all term weighing techniques. Although ME and BW performed better than DIST with SRAA dataset, overall DIST performance is significantly
better in classification with higher accuracy percentage. The log involving techniques performed poorly in comparison with their non-log counterparts but slightly better than KDL.
