Codes for papers:

@ARTICLE{SGNN,
  author={Yu, Wenhui and Lin, Xiao and Liu, Jinfei and Ge, Junfeng and Ou, Wenwu and Qin, Zheng},
  journal={IEEE Transactions on Knowledge and Data Engineering}, 
  title={Self-Propagation Graph Neural Network for Recommendation}, 
  year={2022},
  volume={34},
  number={12},
  pages={5993-6002},
}

This project is for our model LCFN and baselines.

* Environment:
  Python 3.6.15 :: Anaconda, Inc.
* Libraries:
  tensorflow 1.12.0
  numpy 1.16.4
  scipy 1.5.2
  pandas 1.1.5
  openpyxl 2.3.2
  xlrd 1.0.0
  xlutils 2.0.0

Please follow the steps below:
1. Pretraining
    1.1 Run _hypergraph_embeddings.py in folder pretraining.
    1.2 Run _graph_embeddings.py in folder pretraining.
    1.3 Run _main.py in folder pretraining (set EMB_DIM as 128, 64, 42, and 32 in p_params.py).
    We also provide downloading for pretraining:
        https://drive.google.com/file/d/1UV3KO_5wOKkr4v5FePD19cVGhGifz4SR/view?usp=sharing
        https://pan.baidu.com/s/1KuI4gHViONl3tzRT1Prv1w (password: 1234)
    You can choose one of these two URLs for downloading (we recommend the first one). Downloaded and unzip LCFN_dataset.zip, and use it to replace the folder dataset in our project.

2. Run _main.py in our project (datasets, hyperparameters can be set in params.py).
    2.1 Tuning models (if you want to change datasets or hyperparameters): We provide a automatic tool to tune models with respect to learning rate \eta and regularization coefficient \lambda. Set "tuning_method" in line 24 in _main.py as 'tuning' and run _main.py. The best \eta and \lambda and corresponding performance can be returned.
    2.2 Testing models: Set "tuning_method" as 'test' and run _main.py.

3. Check results in folder experiment_result. Collect results by result_collection.

******************************************************************************

* In the result_collection folder, we provide a tool for results collection. Please read the manual for details.

* We also release our tuning results in folder supplementary_material.

* In the dataset folder, we prodive Amazon and Movielens to conduct our experiments. For each dataset, we split it to three subsets: train_data, validation_data, and test_data. You can use our processed datasets, or construct them from the raw data by running amazon.py and movielens.py. For the raw data please find on:

1. Amazon 
http://snap.stanford.edu/data/amazon/productGraph/categoryFiles/reviews_Electronics_5.json.gz

2. Movielens
http://grouplens.org/datasetss/movielens/1m

******************************************************************************

