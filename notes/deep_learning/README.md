
### Transfer Learning
The most common incarnation of transfer learning in the context of deep learning is the following workflow:
- Take layers from a previously trained model.
- Freeze them, so as to avoid destroying any of the information they contain during future training rounds.
- Add some new, trainable layers on top of the frozen layers. They will learn to turn the old features into predictions on a new dataset.
- Train the new layers on your dataset.
https://keras.io/guides/transfer_learning/