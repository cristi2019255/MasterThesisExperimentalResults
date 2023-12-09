# MasterThesisExperimentalResults

This repository stores the Experimental Results for the Master Thesis of Grosu Cristian 2023 entitled "Decision Boundary Maps for supporting user-driven pseudo-labeling"

## Structure of this repository

- experiments_results
  - DBM_optimization_heuristics
    - hyperparamter_tunning
      - number_of_blocks_B
        - PCA [1]
        {********************************
          - binary_split [2]
            {********************************
            - img
              - B.npy (the result for the experiment with the hyperparameter B)
            - experiment_results.txt (the runtimes taken for generating the DBM with each hyperparameter value of B)
            - label_errors.txt (the relative amount of label errors for the DBM with each hyperparameter value of B)
            ********************************}
          - confidence_interpolation
            - [2]
        ********************************}
        - t-SNE
          - [1]
        - UMAP
          - [1]
        - autoencoder
          - [1]
        - ssnp
          - [1]
        - aggregates (.png images representing aggregates of the results)
    - results
      - ..
  - tool_usage_evaluation
    - MNIST (the results when using the MNIST data set)
      - user1_GrosuCristian (the results achieved by user 1)
        - ...
      - user2_BarbaraBenato (the results achieved by user 2)
        - ...
    - protozoan_cysts (the results achieved when using the protozoan cysts data set)
      - user1_GrosuCristian (the results achieved by user 1)
        - ...
      - user2_BarbaraBenato (the results achieved by user 2)
        - ...
