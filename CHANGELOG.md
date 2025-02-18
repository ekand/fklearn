# Changelog

## [2.0.0] - 2021-12-28
- **Possible breaking changes**
    - Allow greater versions of `catboost`, `lightgbm`, `xgboost`, `shap`, `swifter`
    (mostly due to deprecation of support to Python 3.5 and older versions). Libraries depending on
    `fklearn` can still restrict the versions of the aforementioned libraries, keeping the previous
    behavior.

## [1.24.0] - 2021-12-06
- **New**
    - Add causal curves summary
- **Bug fix**
    - Set correct learner name for learners with column_duplicatable decorator

## [1.23.0] - 2021-10-29
- **New**
    - Add common causal evaluation techniques
    - Add methods to debias a dataframe with a treatment T and confounders X

## [1.22.2] - 2021-09-01
- **Bug fix**
    - Remove `cloudpickle` from requirements

## [1.22.1] - 2021-09-01
- **Bug fix**
    - Remove cloudpickle from parallel_validator

## [1.22.0] -  2021-02-09
- **Enhancement**
    - Add verbose method to `validator` and `parallel_validator`
    - Add column_duplicator decorator to value_mapper
- *Bug Fix*
    - Fix Spatial LC check
    - Fix circleci

## [1.21.0] - 2020-10-02
- **Enhancement**
    - Now transformers can create a new column instead of replace the input
- **Bug Fix**
    - Make requirements more flexible to cover the latest releases
    - split_evaluator_extractor now supports eval_name parameter
    - Fixed `drop_first_column` behaviour in onehot categorizer
- **New**
    - Add learner to calibrate predictions based on a fairness metric
- **Documentation**
    - Fixed docstrings for `reverse_time_learning_curve_splitter` and `feature_importance_backward_selection`

## [1.20.0] - 2020-07-13
- **Enhancement**
    - Now Catboost learner is pickable

## [1.19.0] - 2020-06-17
- **Enhancement**
    - Improve `space_time_split_dataset` performance

## [1.18.0] - 2020-05-08
- **Enhancement**
    - Allow users to inform a Placeholder value in imputer learner
- **New**
    - Add Normalized Discount Cumulative Gain evaluator
- **Bug Fix**
    - Fix some sklearn related warnings
    - Fix get_recovery logic in make_confounded_data method
- **Documentation**
    - Add target_categorizer documentation

## [1.17.0] - 2020-02-28
- **Enhancement**
    - Allow users to set a gap between training and holdout in time splitters
    - Raise Errors instead of use asserts
- **New**
    - Support pipelines with duplicated learners
    - Add stratified split method
- **Bug Fix**
    - Fix space_time_split holdout
    - Fix compatibility with newer shap version

## [1.16.1] - 2020-01-02
- **Enhancement**
    - Increasing isotonic calibration regression by adding upper and lower bounds.

## [1.16.0] - 2019-10-07
- **Enhancement**
    - Improve split evaluator to avoid unexpected errors
- **New**
    - Now users can install only the set of requirements they need
    - Add Target encoding learner
    - Add PR AUC and rename AUC evaluator to ROC AUC
- **Bug Fix**
    - Fix bug with space_time_split_dataset fn
- **Documentation**
    - Update space time split DOCSTRING to match the actual behaviour
    - Add more tutorials(Pydata)

## [1.15.1] - 2019-08-16
- **Enhancement**
    - Now learners that have a model exposes it in the logs as `object` key

## [1.15.0] - 2019-08-12
- **Enhancement**
    - Make `custom_transformer` a pure function
    - Remove unused requirements
- **New**
    - Now features created by one hot enconding can be used in the next steps of pipeline
    - Shap multiclass support
    - Custom model pipeline
- **Bug Fix**
    - Fix the way one hot encoding handle nans
- **Documentation**
    - Minor fix flake8 documentation to make it work in other shells
    - Fix fbeta_score_evaluator docstring
    - Fix typo on onehot_categorizer
    - New tutorial from meetup presentation

## [1.14.0] - 2019-04-30
- **Enhancement**
    - Validator accepts predict_oof as argument
- **New**
    - Add CatBoosting regressor
    - Data corruption(Macacaos)
- **Documentation**
    - Multiple fixes in the documentation
    - Add Contribution guide

## [1.13.4] - 2019-04-25
- **Enhancement**
    - Add predict_oof as argument to validator

## [1.13.3] - 2019-04-24
- **Bug Fix**
    - Fix warning in `placeholder_imputer`

## [1.13.2] - 2019-04-10
- **Bug Fix**
    - Fixing missing warner when there is no row with missing values

## [1.13.1] - 2019-04-10
- **New**
    - Add missing warner transformation

## [1.13.0] - 2019-04-01
- **New**
    - Add public version code
