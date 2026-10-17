# CNN Retinal OCT Classification

I wanted to apply the neural network concepts I learned in class to medical images. This project uses PyTorch and [OCTMNIST](https://medmnist.com/) to classify retinal OCT scans into four categories: CNV, diabetic macular edema, drusen, and normal.

The notebook compares a fully connected network with two small CNNs, one with a single convolutional layer and one with two. The goal is to see how they compare in classification performance, number of parameters, and training time.

The code uses the dataset's training, validation, and test splits. Checkpoints are selected using validation loss. Evaluation includes accuracy, macro-F1, recall for each class, confusion matrices, and examples of incorrect predictions.

Training and evaluation on OCTMNIST are still pending. The code has been checked using synthetic data, but there are no OCTMNIST results yet. This is a learning project, not a tool for clinical use.

## Running it

Install the dependencies in `requirements.txt`, then open `CNN Retinal OCT Classification.ipynb` in VS Code or Jupyter with that Python environment selected. For GPU support, install a compatible build of [PyTorch](https://pytorch.org/get-started/locally/) first.

The switches near the top of the notebook are off by default. Set `LOAD_DATA` and `RUN_TRAINING` to `True` to load the data and train the models. Once training is finished, turn `RUN_TRAINING` off and enable `RUN_TEST_EVALUATION` with the same configuration and run name. Run the cells in order from the project folder.

Data downloads and saved results stay local and are excluded from Git.

## References

- [MedMNIST v2 paper and dataset](https://doi.org/10.1038/s41597-022-01721-8)
- [Original retinal OCT study — Kermany et al.](https://doi.org/10.1016/j.cell.2018.02.010)
