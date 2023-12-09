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
        - train_0.2
          - DBM_PCA
            - plot_snapshots (the tool view after each usage iteration)
              - date.png | date_revoked.png (this means this iteration was undone)
            - refit-classifier (the classifier generated after the tool usage)
            - classifier_accuracy.png (the classifier accuracy change over the iterations)
            - classifier_kappa_score.png (the classifier Cohen's kappa score change over the iterations)
            - classifier_performance.log (the classifier performance over the iterations)
            - label_changes.json (the label changes over the iterations)
            - labels_result.npy (the labels after the tool usage)
          - DBM_tSNE
          - DBM_UMAP
          - SDBM_autoencoder
          - SDBM_ssnp
        - train_0.4
        - train_0.6
        - train_0.8
        - train_1.0
        - metadata_acc_improvement (shows how the accuracy of a classifier improved when different projection methods were involved)
        - metadata_kappa_improvement (shows how the Cohen kappa score of a classifier improved when different projection methods were involved)
      - user2_BarbaraBenato (the results achieved by user 2)
        - train_0.2
        - train_0.4
        - train_0.6
        - train_0.8
        - train_1.0
        - metadata_acc_improvement (shows how the accuracy of a classifier improved when different projection methods were involved)
        - metadata_kappa_improvement (shows how the Cohen kappa score of a classifier improved when different projection methods were involved)
    - protozoan_cysts (the results achieved when using the protozoan cysts data set)
      - AuNN (the autoencoder used for feature extraction in the protozoan cysts experiments)
      - user1_GrosuCristian (the results achieved by user 1)
        - t-SNE
          - plot_snapshots (the tool view after each usage iteration)
            - date.png | date_revoked.png (this means this iteration was undone)
          - refit-classifier (the classifier generated after the tool usage)
          - classifier_accuracy.png (the classifier accuracy change over the iterations)
          - classifier_kappa_score.png (the classifier Cohen's kappa score change over the iterations)
          - classifier_performance.log (the classifier performance over the iterations)
          - label_changes.json (the label changes over the iterations)
          - labels_result.npy (the labels after the tool usage)
          - metadata.txt (additional data, statistics about the experiment)
      - user2_BarbaraBenato (the results achieved by user 2)
        - t-SNE
          - plot_snapshots (the tool view after each usage iteration)
            - date.png | date_revoked.png (this means this iteration was undone)
          - refit-classifier (the classifier generated after the tool usage)
          - classifier_accuracy.png (the classifier accuracy change over the iterations)
          - classifier_kappa_score.png (the classifier Cohen's kappa score change over the iterations)
          - classifier_performance.log (the classifier performance over the iterations)
          - label_changes.json (the label changes over the iterations)
          - labels_result.npy (the labels after the tool usage)
          - metadata.txt (additional data, statistics about the experiment)
      - comparison aggregates
