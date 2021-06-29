# Endometrial cancer study data

Model data developed with scikit-learn for the classification of endometrial cancer using radiomics data from T2-weighted MRI images.
The "Files" folder contains the trained model ("SVM.pkl") that can be employed on new data prepared following the study processing pipeline.

# Preparing the data

The model was trained on radiomic data extracted using [PyRadiomics](https://pyradiomics.readthedocs.io/en/latest/). Using whole-lesion masks and the settings file ("params.yaml") included in the repository, an appropriate test set can be obtained from any endometrial cancer MRI exam including T2-weighted images.
The extracted data should then be scaled by using the pickled Python objects also included in the repository. The pickled feature list ("features_scaler.pkl") contains the feature set on which to apply the scaler, while the scaler object ("scaler.pkl") contains the scikit-learn MinMaxScaler that can be loaded and fitted to the new data.
Finally, from the resulting, scaled dataset the features actually employed to train the model should be selected (included in the "features_model.pkl" file). The resulting data can now be used by the SVM model to obtain new predictions.

## Citation

Will update with paper details as soon as possible.

## License

Creative Commons Attribution 4.0 International (CC-BY-4.0). See "LICENSE" file for full details.
