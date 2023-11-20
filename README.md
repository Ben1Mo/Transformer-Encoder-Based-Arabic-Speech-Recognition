# Transformer-Encoder-Based-Arabic-Speech-Recognition
This repository holds the implementation for the paper: "Transformer for Arabic Speech Commands Recognition using fine-tuning Hyperparameter and data augmentation Technique"

## Dataset

The *"Arabic Speech Commands Dataset"*, used within this work, is imported from [this repository](https://github.com/abdulkaderghandoura/arabic-speech-commands-dataset).

### Classes

The following classes are used:

```
classes = ["zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine","right", 
 	   "left", "up", "down", "forward", "backward", "yes", "no", "stop", "start", "enable", 
 	   "disable", "ok", "cancel", "open", "close", "zoom in", "zoom out", "previous", "next", 
 	   "send", "receive", "move", "rotate", "record", "enter", "digit", "direction", "options", "undo"]
```

### Configuration

You can follow these steps to start testing the `AudioSpectogram.ipynb` notebook:

1. Create a Python virtual environment,e.g: following this [link](https://virtualenv.pypa.io/en/latest/user_guide.html).
2. Install requirements, running the following:
```
pip install -r requirements.txt
```
3. Configure Jupyter Notebook to include you created virtual env following the steps in these [docs](https://ipython.readthedocs.io/en/stable/install/kernel_install.html#kernels-for-different-environments).
4. Run the jupyter notebook, choose the right kernel from the list of kernels in the notebook configuration.
5. Have fun!
