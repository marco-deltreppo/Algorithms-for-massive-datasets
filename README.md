# Algorithms-for-massive-datasets
The task is to implement a detector of pairs of similar items, analyzing the "325 Bird Species" dataset published on Kaggle. The detector must consider the images in the dataset and output the pairs inferred as similar.

- The major goal of finding candidate pairs was accomplished in a for loop using the list of all paths as reference. The subsequent steps were done for all the 50582 images. 

- Convert the image to gray scale and resize to 17 X 16. Compute the "signature" of the image using dHash. For each band of 51 binary values of the signature compute the hash using .tobytes() and map to the respective bucket.

- From all the buckets with more than one item is possible to create the candidate set of pairs. For each pair of the candidate set is than computed the xor similarity to check if the candidate are similar or just false positive. 

The solution is written with Python 3 in Google Colab for easier reproducibility of the results. The link to run the code can be found by clicking on the Near_Duplicate.ipynb file of this Github repository where there will be a button directing the user to Colab. Alternatively, you can directly click on the button here: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/marco-deltreppo/Algorithms-for-massive-datasets/blob/main/Near_duplicate.ipynb)
. Once connected to the "Python 3 Google Compute Engine backend" it will be sufficient to upload your personal Kaggle API token in the dedicated section of the notebook.
