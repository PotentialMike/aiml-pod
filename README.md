```
chmod +x ~/Downloads/Miniforge3-MacOSX-arm64.sh
sh ~/Downloads/Miniforge3-MacOSX-arm64.sh
source ~/miniforge3/bin/activate
```

Make dev directory

```
mkdir DIRECTORY_NAME
cd DIRECTORY_NAME
```

Python 3.8 is supposed to be most stable

```
conda create --prefix ./env python=3.8
conda activate ./env
```

Install libs

- Apple-flavored dependencies
- Base TensorFlow
- Leverage Apple Metal

```
conda install -c apple tensorflow-deps
python -m pip install tensorflow-macos
python -m pip install tensorflow-metal
```

Optional

```
python -m pip install tensorflow-datasets
```

Common Libraries

```
conda install jupyter pandas numpy matplotlib scikit-learn
```

Optional: launch Jupyter Notebook

```
jupyter notebook
```

Sample code to check it out

```
import numpy as np
import pandas as pd
import sklearn
import tensorflow as tf
import matplotlib.pyplot as plt

# Check for TensorFlow GPU access
print(f"TensorFlow has access to the following devices:\n{tf.config.list_physical_devices()}")

# See TensorFlow version
print(f"TensorFlow version: {tf.__version__}")
```
