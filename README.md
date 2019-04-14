# Classical Piano Composer for emotions
This is a forked project to train a neural network to generate midi music files that make use of a single instrument. This projects is adapted so that music is generated with an emotional label 'happy', 'sad', 'anger', or 'surprise'.

## Requirements

* Python 3.x
* Installing the following packages using pip:
	* Music21
	* Keras
	* Tensorflow
	* h5py

## Training

To train the network you run **lstm.py emotion number_of_songs**.

emotion only contains: 'happy','sad','anger' and 'surprise'
number_of_songs: how many songs based to generate the music 

E.g.

```
python lstm.py 'happy' 15
```

The network will use every midi file in ./midi_songs to train the network. The midi files should only contain a single instrument to get the most out of the training.

**NOTE**: You can stop the process at any point in time and the weights from the latest completed epoch will be available for text generation purposes.

## Generating music

Once you have trained the network you can generate text using **predict.py emotion**

E.g.

```
python predict.py 'happy'
```

You can run the prediction file right away using the **weights.hdf5** file
