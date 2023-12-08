# Ancient Handwritten Recognition under data deficient condition

To run the pickle file to get the accuracy that we mentioned in the results. Please follow these steps.  

You need anaconda install in your system.
Then create an environment 
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

Now for running the code. 
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

This command generates new images:
```
python main.py -dg --save_dir emnist_bal_200/ -w emnist_bal_200/trained_model.h5 --samples_to_generate 10
```
10 here is the number of samples to generate. 