# Usage and Citation
If you use this data, please cite

Schirmer, Markus D., et al. "Neuropsychiatric disease classification using functional connectomics-results of the connectomics in neuroimaging transfer learning challenge." Medical image analysis 70 (2021): 101972.

https://www.sciencedirect.com/science/article/abs/pii/S1361841521000189

# 2019_CNI_TrainingRelease
Training data release for Connectomics in NeuroImaging - Transfer Learning Challenge (CNI-TLC). For more details, see http://miccai.brainconnectivity.net

# Challenge Data

The data used for this challenge consists of preprocessed time resting-state fMRI (rs-fMRI) time series and demographic information. The rs-fMRI data was acquired on a Phillips 3T Achieva scanner using a single shot, partially parallel gradient-recalled EPI sequence with TR/TE = 2500/30ms, flip angle 70, voxel resolution = 3.05 x 3.15 x 3mm, and a duration of either 128 or 156 time samples. Subjects were instructed to relax with their eyes open and focus on a central cross-hair, while remaining still for the duration of the scan.

Preprocessing includes slice time correction, rigid body realignment, and normalization to the EPI version of the MNI template. The time courses were temporally detrended in order to remove gradual trends in the data. CompCorr (Behzadi et al. 2007) was performed to estimate and remove spatially coherent noise from the white matter and ventricles, along with the linearly detrended versions of the six rigid body realignment parameters and their first derivatives. From here, the data was spatially smoothed with a 6mm FWHM Gaussian kernel and bandpass filtered between 0.01-0.1 Hz. Finally, spike correction was performed using the AFNI package (Cox et al. 1996), as an alternative to motion scrubbing.

For this challenge, we have extracted the mean time courses of the preprocessed rs-fMRI data using three standard parcellations: AAL (116 ROIs), Harvard Oxford (110 ROIs) and Craddock200 (200 ROIs). The data for each parcellation is included as a separate timeseries_XXX.csv file in corresponding the subject directory. Here, rows correspond to parcel number and columns correspond to time samples. Participants are free to use any of this data to develop their models.

In addition to the rs-fMRI data, we will provide the following demographic variables for each subject: Age, Sex, FSIQ, and Edinburgh Handedness. This information can be found in the accompanying phenotypic.csv file in each subject directory. During training and validation, we will provide diagnosis (DX) for participants to evaluate their models. During testing, the DX field will contain N/A.

#Related data releases

Training data: https://github.com/mdschirmer/2019_CNI_TrainingRelease

Validation data: https://github.com/mdschirmer/2019_CNI_ValidationRelease

Test data: https://github.com/mdschirmer/2019_CNI_TestRelease
