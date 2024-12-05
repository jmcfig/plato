# Replication process

## Installation w/ additional notes

To begin with the replication process we first need to create a environment with all the necessary packages in certain versions, and let me tell you - that was not easy to figure out!

Start by creating a virtual environment in python 3.6.

```conda create -n plato python==3.6```

Then you need to install all required packages:

```pip install -e .```

If there are any version conflicts, make sure to install the lowest version present in requirements.txt.

For example: ```ludwig>=0.2.2``` -> ```pip install ludwig==0.2.2```

Tensorflow may also cause problems. So we recommend to try version 1.15 as it should work fine.

