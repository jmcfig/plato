# TSI - Multi agent research dialogue system

To use the same methods as the researchers who posted the paper ------ , ------, ------. We used plato, developed by UberAI (which they work for).

## Installation w/ additional notes

To begin with the replication process we first need to create a environment with all the necessary packages in certain versions, and let me tell you - that was not easy to figure out!

Start by creating a fresh environment in python 3.6. We used anaconda, you may use python virtual environments if preferred.

```conda create -n plato python==3.6```

Then you need to install all required packages. Go to the plato-research-dialogue-system-master directory and run the following line:

```pip install -e .```

If there are any version conflicts, installing the lowest version present in requirements.txt should fix them.

For example: ```ludwig>=0.2.2``` -> ```pip install ludwig==0.2.2```

Tensorflow may also cause problems. So we recommend to try version 1.15, which should work fine.



### Running tutorial

The main tutorial was not great, so let's dive deeper into each step we should take to train the multi agent system.

#### Parsing the data

Go to https://github.com/matthen/dstc and download dstc2_traindev.tar.gz.

Then run the following command:

Go to `example/config/parser/Parse_DSTC2.yaml` and change the data_path to where you extracted the data mentioned above.

Then run:

```plato parse -config 'Parse_DSTC2.yaml'.```

If it doesn't work try with the full path to the yaml file:


```plato parse -config example/config/parser/Parse_DSTC2.yaml.```


Check the data folder to see if it worked. It should have created the following files:

![alt text](images/data_parsed.png)


