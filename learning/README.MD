# README



## keras 1.2.x upgrade to keras 2.x

https://github.com/keras-team/keras/issues/5870
https://forums.fast.ai/t/keras-2-released/1956

Keras 1.x -> Keras 2.x
Keras 1.x:

#1 from keras.layers.convolutional import Convolution2D
#2 from keras.regularizers import l2, activity_l2, l1, activity_l1
#3 from keras.utils.layer_utils import layer_from_config
#4 from keras import backend
#5 Convolution2D
#6 batches.nb_sample
#7 batches.nb_class
#8 model.add(Convolution2D(filters, 3, 3, activation="relu"))
#9 fit_generator(batches, samples_per_epoch=batches.nb_sample, nb_epoch=nb_epoch, validation_data=val_batches, nb_val_samples=val_batches.nb_sample)
#10 nb_epoch
#11 self.model.predict_generator(test_batches, test_batches.nb_sample)

Keras 2.x:

#1 from keras.layers.convolutional import Conv2D
#2 from keras.regularizers import l2, l1
#3 from keras.layers import deserialize as layer_from_config
#4 from keras import backend; backend.set_image_dim_ordering('th')
#5 Conv2D
#6 batches.samples
#7 batches.num_class
#8 model.add(Conv2D(filters, (3, 3), activation="relu"))
#9 fit_generator(batches, steps_per_epoch=batches.samples//batches.batch_size, epochs=nb_epoch, validation_steps=val_batches.samples//val_batches.batch_size)
#10 epochs
#11 self.model.predict_generator(test_batches, test_batches.samples//test_batches


## python3

install PIL

sudo pip install Pillow

cPickle is pickle