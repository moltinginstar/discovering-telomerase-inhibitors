# Discovering telomerase inhibitors with machine learning

This is a group[†](#acknowledgments) project I did for my undergraduate machine learning class. The goal was to use machine learning to find new telomerase inhibitors. Telomerase is an enzyme that plays a key role in cancer cell immortality, and blocking it is a promising strategy for cancer treatment.

I was really impressed by a recent paper by [Vanessa Smer-Barreto et al.](https://www.nature.com/articles/s41467-023-39120-1) that used remarkably simple machine learning techniques to discover novel anti-aging drugs, and I thought it would be interesting to try and replicate their approach for a different target.

I constructed a dataset of known telomerase inhibitors and non-inhibitors and used it to train a machine learning model to predict the activity of new molecules. I then used the model to screen a large database of molecules to find new telomerase inhibitors (with some success!).

## Project structure

- [`data/`](data)
  - [`data.csv`](data/data.csv): the final training set, consisting of 50 positive and 2977 negative samples
  - [`screen.csv`](data/screen.csv): the final screening library, containing 1683 biologically active molecules
  - [`fda.csv`](data/fda.csv): the Selleck FDA-Approved Drug Library, the source of the negative samples
  - [`prestwick_lopac.csv`](data/prestwick_lopac.csv): a dataset assembled from the Prestwick Chemical Library® and the LOPAC®1280 library, the main source of the screening data
  - [`CB61365618.mol`](data/CB61365618.mol): the structure of the telomerase inhibitor 2-(3-(trifluoromethyl)phenyl)-isothiazolin-3-one
- [`data.ipynb`](data.ipynb): the notebook used to collect and preprocess the data
- [`main.ipynb`](main.ipynb): the main notebook, containing data cleaning, model training, and screening

## Acknowledgments

Everything in this repository is my own work, except for the data, which was collected from publicly available sources. My group members simply presented it to the class alongside me. I ❤️️ college group projects.

Credit goes to the authors of the [Discovery of senolytics using machine learning](https://www.nature.com/articles/s41467-023-39120-1) paper for the idea, and to the developers of the tools and libraries I used, including [`RDKit`](https://www.rdkit.org/), [`scikit-learn`](https://scikit-learn.org/stable/), and [`pandas`](https://pandas.pydata.org/), for making this project relatively painless.

For a full list of references and acknowledgments, see the main notebook.
