### Checkpoint Keras 

The example implementation of Keras model shows how the save a checkpoint of trained model and then load it from the file. 

## Save the checkpoint
`‌checkpoint_cb = keras.callbacks.ModelCheckpoint("YOURS-MODEL-NAME.h5", save_best_only=True)`

## Checkpoint callback after each epoch
`‌history = model.fit(X_train, y_train, epochs = 50, validation_data=(X_valid, y_valid), callbacks=[checkpoint_cb])`

## Load the model
`loadedModel = keras.models.load_model("YOURS-MODEL-NAME.h5")`