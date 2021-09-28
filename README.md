stroke-prediction
Stroke infarct growth prediction (3D, PyTorch 0.3)

Objective
Learning to Predict Stroke Infarcted Tissue Outcome based on Multivariate CT Images

Data
The source code is working from within the IMI network at University of Luebeck, as the closed dataset of 29 subjects is only accessable if you are member of the bvstaff group. The filenames have been renamed and cases are represented as a subfolder. CTP modalities CBV and TTD are used as input, corresponding manual segmentations for core and penumbra, as well as follow-up lesion segmentation (FUCTMap). The directory contains more files since the work for the Master's thesis of Linda Aulmann.

The dataset specified in data.py is inherited from torch.utils.data.Dataset, thus can be exchanged with other datasets and loaders (At the moment there are two datasets with different transformations for training and validation). The existing Learners expect 3D pytorch tensors of shape BxCxDxHxW, but implementing an own Learner will enable the use of 2D data as well.
