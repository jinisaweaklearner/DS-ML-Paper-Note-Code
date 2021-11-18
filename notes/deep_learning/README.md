## Deep Learning overview
- 
- Co
- Sequential model (e.g. RNN, LSTM)
-

### Transfer Learning
The most common incarnation of transfer learning in the context of deep learning is the following workflow:
- Take layers from a previously trained model.
- Freeze them, so as to avoid destroying any of the information they contain during future training rounds.
- Add some new, trainable layers on top of the frozen layers. They will learn to turn the old features into predictions on a new dataset.
- Train the new layers on your dataset.
https://keras.io/guides/transfer_learning/

# Keras
- freeze and fine-tuning https://keras.io/guides/transfer_learning/#transfer-learning-amp-finetuning
- get weights for each layer https://stackoverflow.com/questions/46817085/keras-interpreting-the-output-of-get-weights
- set weights https://stackoverflow.com/questions/51354186/how-to-update-weights-manually-with-keras
- layer weight regularizers https://keras.io/api/layers/regularizers/#l1-class
- layer weight constraints https://keras.io/api/layers/constraints/
- weight contraints example https://machinelearningmastery.com/how-to-reduce-overfitting-in-deep-neural-networks-with-weight-constraints-in-keras/
- all constraints https://www.tensorflow.org/api_docs/python/tf/keras/constraints