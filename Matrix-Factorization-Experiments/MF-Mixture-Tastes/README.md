# Matrix Factorization for Collaborative Filtering with Mixture of Tastes

This is my PyTorch implementation of a Matrix Factorization model for Collaborative Filtering. This model includes a mixture of tastes.

## Requirements
```
PyTorch 1.3 & Python 3.6
Numpy
Pandas
Pytorch-Ignite
Sklearn
TensorboardX
```

## Scripts
* [MFMixTaste.py](https://github.com/khanhnamle1994/transfer-rec/blob/master/Matrix-Factorization-Experiments/MF-Mixture-Tastes-CF-PyTorch/MFMixTaste.py): This is the model script that defines the Matrix Factorization model with biases.
* [train.py](https://github.com/khanhnamle1994/transfer-rec/blob/master/Matrix-Factorization-Experiments/MF-Mixture-Tastes-CF-PyTorch/train.py): This is the main training script. You can simply run `python train.py` to execute it.

## Results
The full results are stored in [this folder](https://github.com/khanhnamle1994/transfer-rec/tree/master/Matrix-Factorization-Experiments/MF-Mixture-Tastes-CF-PyTorch/results). After training the model for 50 epochs, I got the training loss MSE = 0.609 and validation accuracy = 0.817.

## Run Tensorboard in the background
While I am using PyTorch instead of Tensorflow directly, the logging and visualization library Tensorboard is an amazing asset to track the progress of our models. It's implemented as a small local web server that constructs visualizations from log files, so start by kicking it off in the background:

```
tensorboard --logdir runs
```

Visit the Tensorboard dashboard by going to [http://localhost:6006](http://localhost:6006)

<img src="https://github.com/khanhnamle1994/transfer-rec/blob/master/Matrix-Factorization-Experiments/MF-Mixture-Tastes-CF-PyTorch/loss_mse.png" width="500" /><img src="https://github.com/khanhnamle1994/transfer-rec/blob/master/Matrix-Factorization-Experiments/MF-Mixture-Tastes-CF-PyTorch/valid_accuracy.png" width="500" />