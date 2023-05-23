# Auto-Music-Tag-Generation :notes: :guitar: :headphones:	

#### A project that can Automatically generating music tags

#### To play with this demo, you can go to this :point_right: [colab link](https://colab.research.google.com/drive/10hhthqFWaMbe_oWFYN2nw12uTNYBAYgc?usp=sharing) :point_left:	or *clone this repo and follow the steps* to play with this project. :point_down:	:point_down:	

## Our model structure (Seq2seq):
* **Input**: Music data --> Spectrogram data
* **Encoder**: one CNN layer and one LSTM layer (Spectrogram data --> latent vector)
* **Decoder**: LSTM (latent vector --> Text vector)
* **Output**: Text vector --> Music aspect text

<img width="1009" alt="Screenshot 2023-04-27 at 23 23 00" src="https://user-images.githubusercontent.com/78404109/235127908-c2a570c9-5fff-4a68-8d70-11ee61907baa.png">

## Clone this repo:
``` 
git clone https://github.com/allent4n/auto-music-tag
```

## Dataset (1000 of music data)

Given the MusicCaps data from this link (https://www.kaggle.com/datasets/googleai/musiccaps), a subset of music data (1000 music data) has been sampled for our baseline model training, the sampled music data can be downloaded from:

```
https://liveln-my.sharepoint.com/:f:/g/personal/allentan_ln_hk/ErUL0UhQgHBAtn8O16FZvUwBfoET5grtnqQnZqHYY9rN7Q?e=ePqhL2
```
The data link contains **1000 music data samples**:
* You can download all data for training or you can simply download 10 to simply run and play with the model


## Environment
Run the following codes to build a virtual environment for this project:
```
mkdir venv
virtualenv -p python3 venv/
source venv/bin/activate
pip install -r requirements.txt
```


## Training
### Pre-training 
* place go to the auto-music-tag folder and generate a new folder, you can do it by the following codes:
```
cd auto-music-tag
mkdir 1k_data
```
* Then put your downloaded data into the **1k_data** folder.

### train the model

* run the following code to train the model
```
python music2aspect.py
```

## Testing 
* You can either download the trained model parameters from the following link or train your own model:
```
https://liveln-my.sharepoint.com/:f:/g/personal/allentan_ln_hk/ErT8ToNqyuxIkSkpcn3b1e4BB3ma9E2bD71R1hiTYLtvhw?e=lJ6hOB
```
* Then run this code to visualize the possible tags for the testing music
```
python inference.py
```
# Enjoy :clinking_glasses:	:clinking_glasses:	
