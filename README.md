TBR Models
==========

This repository contains machine learning models trained on the data produced by the tritium breeding ratio Monte Carlo simulation.


Usage
-----

The repository is divided into multiple models, each corresponding to a separate
directory. Directory names are comprised of underscore-separated tokens:

  1. token represents a sequential number of the model,
  2. token refers to training set type:
    - `1slice` means a single slice of discrete parameters,
    - `all` means all slices of discrete parameters,
  3. token identifies the run from which the training set originates,
  4. token identifies the first batch of the run (inclusive),
  5. token identifies the last batch of the run (exclusive),
  6. token determines the model type,
  7. token (and onwards) provide information about model configuration and
     hyperparameters, they vary depending on the model type.

In each directory, the following files are usually found:

  - `train_command` ... contains the shell command used to produce the model
    (note that some parameters may have been added to the training utility since it was last used)
  - `test_performance.{png,pdf}` ... shows the scatter plot of true vs.
    predicted TBR
  - `training.log` ... contains output of the training session (including
    model's evaluation on the testing set)

Other files depend on the model type.

License
-------

This work was realised in 2020 as a group project at University College London with the support from UKAEA. The authors of the implementation are Petr Mánek and Graham Van Goffrier.

Permission to use, distribute and modify is hereby granted in accordance with the MIT License. See the LICENSE file for details.
