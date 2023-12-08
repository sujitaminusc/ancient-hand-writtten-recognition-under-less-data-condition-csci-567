# Ancient Handwritten Recognition under data deficient condition

# Goal
The primary goal of this project is to significantly improve the accuracy of handwritten character recognition for ancient indian languages under very less data samples per class. Since these languages have historically faced challenges due
to the scarity availability of labeled data. We aim to develop an innovative approach that leverages Capsule Networks to address this issue and achieve state-of-the-art
performance with 190 training samples per character. By doing so, we seek to enable more comprehensive analysis and interpretation of historical texts. This project holds considerable importance as
it addresses a longstanding problem in the field of character recognition. Ancient languages, being a crucial part of our cultural heritage, often lack extensive labeled datasets. Consequently, existing
methods struggle to provide accurate character recognition, impeding historical research and preservation efforts. In our research, we introduce a novel approach to address the issue of limited dataset sizes using capsule networks. We leverage Capsule Networks capacity to augment data through manipulation of instantiation parameters. CapsNets not only learn an image’s presence but also its attributes, making them advantageous for character recognition with limited data. Our design modifies the capsule network architecture by substituting the decoder
network from Capsule network research paper with a deconvolutional network and making adjustments to the capsule network. By introducing a controlled level of noise to instantiation parameters, we simulate human like realistic variations, leading to a more effective data generation method compared
to traditional affine transformations this data is auto-fed to the training model. Our system closely matches state-of-the-art results with just 190 data points per character.

# Exceution of Pickle file (hdf5, h5)
We have provided hdf5, h5 file for showing our accuracy. 
To run the pickle file to get the accuracy that we mentioned in the results. Please follow these steps.  

You need anaconda install in your system.
Then create an environment. 
Do a git clone. Go to the root folder of the project.
Then exceute this commands. 
```
conda create --name pickleenv python=3.11.5
```
```
conda activate pickleenv 
```
```
pip install -r require_pickle.txt
```


For getting the accuracy of Sanskrit run
```
python sanskrit_run_pickle.py
```
For getting the accuracy of Tamil run
```
python tamil_run_pickle.py 
```
For getting the accuracy of EMNIST run:
```
python emnist_run_pickle.py
```
# Exceution of Code 

You need to have windows or mac. Certain laptops and OS can't run this code due to chipset and os version issue. 
It is known best to work with macOS 14.1.1 and Intel Chipset.
```
conda create --name myenv python=3.6.8
```

```
conda activate myenv 
```


```
pip install -r requirements.txt
```
To run the code for training. 
```
python main.py --cnt 190
```
here 190 is the number of training samples per class.
After training is completed you can generate new images as required. Just have to provide the count of the image (--samples_to_generate 3) 
This command generates new images:
```
python main.py -dg --save_dir emnist_bal_200/ -w emnist_bal_200/trained_model.h5 --samples_to_generate 10
```
10 here is the number of samples to generate. 