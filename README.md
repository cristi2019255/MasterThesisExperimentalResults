# MasterThesisExperimentalResults

This repository stores the Experimental Results for the Master Thesis of Grosu Cristian 2023 entitled "Decision Boundary Maps for supporting user-driven pseudo-labeling"

## Structure of this repository

- experiments_results (results from the experimental sessions)
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
      - PCA [3]
      {********************************
        - binary_split (the Binary Split algorithm results)
          - experiment_metadata.txt (information about the total run time of all the experiments together)
          - experiment_results.txt (information about the run time the computation of DBM for each resolution)
          - resolutions_experiment.png (run time plot of the DBM computation for each resolution)
          - errors_results.txt (information about the \epsilon_label metric for different resolutions)
          - label_errors_experiment.png (\epsilon_label metric plot)
          - cubic_confidence_errors_results.txt (NRMSE_confidence metric when cubic interpolation for confidence map is involved)
          - linear_confidence_errors_results.txt (NRMSE_confidence metric when linear interpolation for confidence map is involved)
          - nearest_confidence_errors_results.txt (NRMSE_confidence metric when nearest neighbor interpolation for confidence map is involved)
          - confidence_errors_experiment.png (NRMSE_confidence metric plot)
        - confidence_interpolation_cubic (the Confidence Interpolation algorithm results when used with confidence_interpolation = bicubic)
          - experiment_metadata.txt (information about the total run time of all the experiments together)
          - experiment_results.txt (information about the run time the computation of DBM for each resolution)
          - resolutions_experiment.png (run time plot of the DBM computation for each resolution)
          - errors_results.txt (information about the \epsilon_label metric for different resolutions)
          - label_errors_experiment.png (\epsilon_label metric plot)
          - confidence_errors_results.txt (NRMSE_confidence_metric information)
        - confidence_interpolation_linear (the Confidence Interpolation algorithm results when used with confidence_interpolation = bilinear)
          - experiment_metadata.txt (information about the total run time of all the experiments together)
          - experiment_results.txt (information about the run time the computation of DBM for each resolution)
          - resolutions_experiment.png (run time plot of the DBM computation for each resolution)
          - errors_results.txt (information about the \epsilon_label metric for different resolutions)
          - label_errors_experiment.png (\epsilon_label metric plot)
          - confidence_errors_results.txt (NRMSE_confidence_metric information)
        - confidence_interpolation_nearest (the Confidence Interpolation algorithm results when used with confidence_interpolation = nearest neighbor)
          - experiment_metadata.txt (information about the total run time of all the experiments together)
          - experiment_results.txt (information about the run time the computation of DBM for each resolution)
          - resolutions_experiment.png (run time plot of the DBM computation for each resolution)
          - errors_results.txt (information about the \epsilon_label metric for different resolutions)
          - label_errors_experiment.png (\epsilon_label metric plot)
          - confidence_errors_results.txt (NRMSE_confidence_metric information)
        - confidence_split (the Confidence Split algorithm results)
          - experiment_metadata.txt (information about the total run time of all the experiments together)
          - experiment_results.txt (information about the run time the computation of DBM for each resolution)
          - resolutions_experiment.png (run time plot of the DBM computation for each resolution)
          - errors_results.txt (information about the \epsilon_label metric for different resolutions)
          - label_errors_experiment.png (\epsilon_label metric plot)
          - cubic_confidence_errors_results.txt (NRMSE_confidence metric when cubic interpolation for confidence map is involved)
          - linear_confidence_errors_results.txt (NRMSE_confidence metric when linear interpolation for confidence map is involved)
          - nearest_confidence_errors_results.txt (NRMSE_confidence metric when nearest neighbor interpolation for confidence map is involved)
          - confidence_errors_experiment.png (NRMSE_confidence metric plot)
        - none (the Dummy DBM algorithm results)
          - experiment_metadata.txt (information about the total run time of all the experiments together)
          - experiment_results.txt (information about the run time the computation of DBM for each resolution)
        - confidence_errors_confidence_interpolation_experiment.png (NRMSE_confidence metric when comparing the confidence interpolation algorithm)
        - confidence_errors_experiment.png (NRMSE_confidence metric when comparing all the heuristics)
        - label_errors_confidence_interpolation_experiment.png (\epsilon_label metric when comparing DBMs given by the confidence interpolation algorithm)
        - label_errors_experiment.png (\epsilon_label metric when comparing all the heuristics)
        - resolutions_confidence_interpolation_experiment.png (run times taken when comparing different interpolation methods in the confidence interpolation algorithm)
        - resolutions_experiment.png (run times when comparing all the heuristics)
      ********************************}
      - t-SNE
        - [3]
      - UMAP
        - [3]
      - autoencoder
        - [3]
      - ssnp
        - [3]
  - tool_usage_evaluation
    - MNIST (the results when using the MNIST data set)
      - user1_GrosuCristian (the results achieved by user 1)
        - train_0.2 [4]
        {********************************
          - DBM_PCA [5]
          {********************************
            - plot_snapshots (the tool view after each usage iteration)
              - date.png | date_revoked.png (this means this iteration was undone)
            - refit-classifier (the classifier generated after the tool usage)
            - classifier_accuracy.png (the classifier accuracy change over the iterations)
            - classifier_kappa_score.png (the classifier Cohen's kappa score change over the iterations)
            - classifier_performance.log (the classifier performance over the iterations)
            - label_changes.json (the label changes over the iterations)
            - labels_result.npy (the labels after the tool usage)
          ********************************}
          - DBM_tSNE
            - [5]
          - DBM_UMAP
            - [5]
          - SDBM_autoencoder
            - [5]
          - SDBM_ssnp
            - [5]
        ********************************}
        - train_0.4
          - [4]
        - train_0.6
          - [4]
        - train_0.8
          - [4]
        - train_1.0
          - [4]
        - metadata_acc_improvement (shows how the accuracy of a classifier improved when different projection methods were involved)
        - metadata_kappa_improvement (shows how the Cohen kappa score of a classifier improved when different projection methods were involved)
      - user2_BarbaraBenato (the results achieved by user 2)
        - train_0.2
          - [4]
        - train_0.4
          - [4]
        - train_0.6
          - [4]
        - train_0.8
          - [4]
        - train_1.0
          - [4]
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
- explanatory assets (images that are used for explanation in the writing part of the thesis)
  - nn_architectures (the visual representations of the neural network architectures we are using in the tool implementation and experiments)
  - pipelines (several pipelines visual illustrations such as experimental and tool usage pipelines)
