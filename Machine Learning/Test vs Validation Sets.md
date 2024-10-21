three splits:
* **Training** - Train the model
* **Validation** - Tune the model's hyperparameters
* **Test** - Evaluate the final model's performance on unseen data

The **validation set** is a sample of data held back from training your model that is used to give an estimate of model skill while tuning the model's hyperparameters. [The validation dataset is different from the test dataset that is also held back from the training of the model, but is instead used to give an unbiased estimate of the skill of the final tuned model when comparing or selecting between final models](https://machinelearningmastery.com/difference-test-validation-datasets/) [1](https://machinelearningmastery.com/difference-test-validation-datasets/).

The **test set** is a sample of data used to provide an unbiased evaluation of a final model fit on the training dataset. The test set provides the gold standard used to evaluate the model's performance. [It is important that no aspect of the test data is used in any way to train the model, including feature selection](https://machinelearningmastery.com/difference-test-validation-datasets/) [1](https://machinelearningmastery.com/difference-test-validation-datasets/).
