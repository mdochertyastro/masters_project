# Outline: PHAS ML Journal Club

Monday afternoon fortnightly (alternate with _IGR-data ML Club_) to go into depth of ML code or paper. Usually reading material supplied before the day and run by Michael Williams. It is open to all PHAS groups so not GW specific at all. 

[PHAS-ML Shared Google Drive](https://drive.google.com/drive/folders/1xqFDCx1h4TB_Tkh3x86CRVwb4mIrZi34)

# meeting 1 - Monday 5/10/20

---

## My preamble questions

- for NN is there only the 3 types: classification, clustering and regression

  - REGRESSION AND CLASSIFICTION are sim. but they are handwavey but good to get into groups (clustering is different and cant be lumped together)
  - Another hand-wavey group is supervised, semi sup and unsup.
    1. sup - 100 pics, we know all them - train
    2. semi-sup - 100 ims, we know 50, 50 unsure - hope the training is enough to give the labels and we can believe them
    3. unsup - 100 ims, no labels - hope running it through a pre-trained and see what it spits out.

- is it just the activation function of the last layer that determines what 'type' of NN task it uses

  - activation function of the output layer isnt the ONLY diff but it's kinda the MAIN diff!

- for each layer there is w wgiht matrix so is that a weight for each node in the layer?

  - each node has a weight for each input and a singular bias for a single node so the layer has a matrix of vectors (length of n inputs)

- can different types of NNs use the same loss function

- how do I get onto your slack?

- where do you start to decide batch size and epoch number and computing expense

- pyTorch vs tf

- what is learning rate for the optimser
  - how big the step the keep the grad minimising looking for the min from activation function

## Q/A session

- why is ReLU so standardly used?

  - Itertively - worked well so stuck with it (pronounced REEE LOO) replaced the 'standard' tanh before
  - look up the 'vanishing gradient' problem

- why more layers (does it make the NN better)?

  - n layer = depth = more flexibility
  - the individual math operations at the layer node is quite inflexible its mutliplication add a bias
  - single layer needs to be REALLY long to do stuff, whereas a finite number of layers and nodes inside layer does the same job

- ReLu: what does it define how the netrons change?
  - how many the neurons update comes from backprop, the ReLu describes WHEN will the neuron fire.
  - would use a different activation function per layer (not per neuron)
  - choice of activation function depends on task (sigmoid for binary 1,0)

## Tutorial session

- read pyTorch docs for dataLoader and how the work
- class inherits (look up python docs)

- need to put () after activation function to load instance
- need to put model and data on same 'device (GPU) on pyTorch can do this with foo.to(device)

- Steps to do in future:
  - define own activation function
  - create own loss functions

https://join.slack.com/t/phas-ml/shared_invite/zt-h2hniuxz-ZPI_8m49OW3m30TZPbYILg

---

# meeting 2 - Monday 19/10/20

## Pres overview:

Speaker: **Eve Chase**
Paper: [Supernova Photometric Classification Pipelines Trained on Spectroscopically Classified Supernovae](https://arxiv.org/abs/1905.07422)
Slides: [updated with google drive](https://drive.google.com/file/d/1J4qQa6jBj369tD9W5LOtrWXoXDpqjKE9/view)

## Pres notes:

- All ML is done on out-of-the-box Scikit-learn
- Can split supernovae into 2 main classes the loads of subcategories:
  - 1a from binary
  - other (didnt catch the 2nd category)
- alot of work is classifying supernovae but with new instruments we will be classifying a million a year.
- this high number calls for ML techniques to (similar to gravity spy) is to blend ML with human-learning
- 4 methods of 'feature selection' in this paper
- PCA - finding a set of lininear combinations of input paramters where these combinations best describe the behaviour/varience of input data.
- PCA comes from scikitlearn
- augment data set so that each trainig data set has same number of entried for each datagory. This is done as 'data augmentation' can look up `imbalanced-learn` in scikit-learn.
- Multi-Layer Perceptron (MLP) is just a normal NN
- can look up scikitlearn-imbalanced-learn [repo](https://github.com/scikit-learn-contrib/imbalanced-learn)


## Questions:

- over summer used PCA to speed up spectral profile matching and inversions. IS that what the paper is using it for, to speed it up also?



