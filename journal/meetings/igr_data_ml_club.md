# Outline: IGR-data Machine Learning Club

Monday afternoon fortnightly (alternate with PHAS ML Journal CLub) informal catchups for ML chat specific to the IGR-data subgroup. Allows us to go deeper than the Generic IGR-data group meetings (Tuesday fortnightly). The structure will be a lead speaker will present a paper or present what they are currently working on and the rest take notes and ask questions to get a deeper appreciation of what each member in

---

# Meeting 1 - MONDAY 12th October

## Minutes:

- more and more people are converting to pyTorch (its like numpy but for ML) so defos good to learn PyTorch first. Good youtube channel called 'Deep Lizard' for PyTorch for complete beginners

- quote from Christine Simpson: "https://www.youtube.com/watch?v=gZmobeGL0Yg&list=PLZbbT5o_s2xq7LwI2y8_QtvuXZedL6tQU
  that’s a deep learning playlist of the basics you’d use with any machine learning library
  Also I’d recommend setting up miniconda/anaconda to manage your environments for each project you try out (people who use C a lot don’t like it, but python ML people use it a lot)"

- a good toy problem to getting started with signal gen for specific grav waves is CNN image stuff (image datasets), then go onto time series later (for glitch stuff)

- pytorch website for good tutorials: https://pytorch.org/tutorials/

- 3 brown 1 blue for good tuts also https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw

- seems to be that PyTorch is the way forward for a few reasons:

  - PyTorch can change between CPU and GPU

- CVAE is a 'Conditional Variational AutoEncoder' - dont know what that is quite yet!

- https://scikit-learn.org/stable/tutorial/machine_learning_map/index.html for a nice pic

- gravity spy paper accessible and a good way to start looking

- https://iopscience.iop.org/article/10.1088/2632-2153/abb93a GW ML review 2020

- https://www.asimovinstitute.org/neural-network-zoo/

- look up what a GAN is

## Post-meeting Recap:

- Low-level API of PyTorch makes it better for:

  - being the industry standard (christine from edin)
  - converting between CPU and GPU in single line of code
  - Better debugging (with unambiguous error messages)

- Good tutorials and resources:

  - [DeepLizard](https://www.youtube.com/watch?v=gZmobeGL0Yg&list=PLZbbT5o_s2xq7LwI2y8_QtvuXZedL6tQU) for different small tutoiral projects (need conda to make diff envs for each one as they have diff dependencies)
  - [Official PyTorch tutorials](https://pytorch.org/tutorials/)
  - [3brown1blue](https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw)
  - [Network Framework examples](https://www.asimovinstitute.org/neural-network-zoo/)

- To research:
  - what is a GAN
  - what is a CVAE
  - ~~[GW ML September rev.](https://iopscience.iop.org/article/10.1088/2632-2153/abb93a)~~ same GW rev from May 2020 w/HUnter that I already have
  - [x] Look into the gravity spy paper - downloaded it in literture/ML
