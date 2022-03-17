# Ai Terms

The general terms that I'm curious about to learn what are they used for while working on a 'Yolo' Ai model. I'll update this note when I'm learning a new terms.

<br> 

**Epochs**: An Epoch means that Ai has been fed with the entire dataset once. (usually 50 is used)

<br>

**Batch size**: A batch is a set of samples used in one iteration of training. For example, if we have 80 images and we choose a batch size of 16. This means the data will be split into 80 / 16 = batches. Once all 5 batches have been fed through the model, exactyly one epoch will be complete.

<br>

**Learning rate**: Learning rate represents the size of the steps taken which indicates how agressive you’d like to train the Ai. If learning rate increases, the area covered in the search space will increase so we might reach goal (global minimum) faster. However, we can overshoot the target. For small learning rates, training will take much longer to reach optimized weight values.

<br>

**Iterations**: Iterations are the number of batches needed to complete one epoch

<br>

Example for all terms:

```
Total training samples (images) = 3000
batch size = 32
epochs = 500
```
For this example:

- 32 samples will be taken at a time to train the network.
- To go through all 3000 samples it takes 94 (3000/32) iterations -> 1 epoch
- This process continues 500 times (epohcs)

