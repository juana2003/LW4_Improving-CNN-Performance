(https://colab.research.google.com/drive/1yGhPYYtnLI2W4gmE_QAF9cQyRKgA6WgP#scrollTo=XXIylrh7l3bf)

A. Model Evaluation Analysis

1. What were the weakest-performing classes based on the confusion matrix? The weakest-performing classes were Ephedra or Mormon Tea (F1-score: 0.38), Misquite (F1-score:    0.39), Cheesebush (F1-score: 0.44), and Desert Milkweed (F1-score: 0.45), indicating frequent misclassifications.

2. How did Precision, Recall, and F1-score vary across classes? Metrics varied significantly: high for classes like Ocotillo (F1: 0.77), Desert Rose (F1: 0.76), and Ice Plant (F1: 0.75), but low for classes like Ephedra or Mormon Tea (Recall: 0.26) and Misquite (Precision: 0.34), showing inconsistent model performance.

3. What does a low recall indicate in your model? A low recall indicates the model fails to identify a large proportion of actual positive samples for that class, resulting in many false negatives (missed instances).

4. How does AUC score reflect model performance compared to accuracy? AUC provides a more robust measure than accuracy, especially for imbalanced datasets, by evaluating the model's ability to distinguish between classes across all probability thresholds, reflecting its discriminative power.

B. Model Improvement

5. How did data augmentation affect validation accuracy? Data augmentation increased validation accuracy from 0.51 to 0.59 by making the model more robust to input variations and improving generalization to unseen data.

6. Why is Batch Normalization important in CNNs? Batch Normalization stabilizes network activations, mitigating internal covariate shift, allowing higher learning rates, and acting as a regularizer, leading to a more stable and better-performing model.

7. What role did Dropout play in improving your model? Dropout acted as a regularization technique, preventing overfitting by randomly deactivating neurons during training. This forced the model to learn more robust and distributed feature representations, improving generalization.

C. Performance Comparison

8. How did Early Stopping prevent overfitting? Early Stopping prevented overfitting by monitoring validation loss and halting training when performance stopped improving, restoring the best weights to ensure optimal generalization on unseen data.

9. What improvements were observed after modifying the model? After modification, validation accuracy improved from 0.51 to 0.59, macro average precision, recall, and F1-score increased from ~0.50 to ~0.59, and the overall AUC score rose from 0.89 to 0.91.

10. Which enhancement contributed the most to performance improvement? Why? The combination of Improved CNN Architecture and Data Augmentation likely contributed the most. The architecture provided learning capacity, while data augmentation supplied diverse data for better generalization.

11. Did the gap between training and validation accuracy decrease? Explain. No, the gap remained negligibly small, but this indicated a failure of the model to learn anything meaningful (both accuracies were very low), not an improvement in generalization.

D. Explainability (Grad-CAM Integration)

12. How did Grad-CAM help in understanding model predictions? Grad-CAM helped understand model predictions by generating heatmaps on input images, visually highlighting the specific regions or features that most influenced the CNN's classification decision.

13. How can the insights from Grad-CAM be used to further improve the model or the dataset? Grad-CAM insights can guide improvements by revealing if the model focuses on irrelevant background features or only parts of an object. This can inform targeted data augmentation, removal of noisy samples, or refinement of model architecture to emphasize correct feature learning.

14. What is the real-world importance of model interpretability techniques like Grad-CAM? Model interpretability, especially via Grad-CAM, is crucial for building trust, debugging model failures (e.g., if a model focuses on a watermark instead of the object), and ensuring fairness and reliability in critical applications like healthcare or autonomous driving.

