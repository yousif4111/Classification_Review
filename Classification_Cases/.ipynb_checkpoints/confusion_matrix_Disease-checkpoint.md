## Example Case: Choosing the Right Metric

### Accuracy
---
**Accuracy:**

Measure the correct predictions made by the model.

Accuracy = (TP + TN)/(TP + TN + FP + FN)

*Example Case:* Accuracy is not suitable because if the model predicts every data point as healthy, the accuracy will be 99%. However, it's a useless model to detect the disease because it labels everybody as healthy, and this metric can be deceptive.

### Recall (Sensitivity)
---
**Recall (Sensitivity):**

Measure the model's ability to classify positive instances.

Recall = TP / (TP + FN)

*Example Case:* If the model classifies everybody as healthy (TN, FN), the Recall will be 0, indicating poor performance. However, Recall alone is not sufficient because if the model classifies everyone as having the disease (TP, FP), there will be no FN, and Recall will be 1, giving an incorrect impression of the model's performance.

### Precision
---
**Precision:**

Measure the model's ability to correctly classify positive instances out of all positive predictions only.

Precision = TP / (TP + FP)

*Example Case:* If the model classifies everyone as positive (diseased) (TP, FP), Precision will be low, close to 0, signaling that the model is flagging everyone as having the disease, which is not desirable. However, Precision faces a similar issue as Recall; it is not sufficient on its own because if the model predicts all as healthy, Precision will be unidentifiable because no patients are flagged as positive.

### Precision-Recall Curves (AUC-PR)
---
Precision-recall curves provide insights into how well a model can correctly identify positive instances (recall) while maintaining a low rate of false positives (precision).
