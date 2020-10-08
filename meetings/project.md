# Meeting 1 - 1/10/20

## Pre-meeting:

## Meeting Minutes:

- Looking at compact binary blackhole mergers
- Old school techniques - MCMC and matched filtering (complete in order of days - week)

- My aim is to eventually be a front-end vit_b developer

- 2 main problems with vit (my project is to fix as many of these as poss):
  1. DATA-RATE - make wavefront longer for NS obs.
  2. NOISE
  3. (Optional) convert vitamin from tf2 to torch

## Post-meeting tasks:

- Bayesian theory research more what is a prior, posterior, likelihood etc

## Questions for next meeting:

- can i get added to ligo wiki or need ligo credentials? (the wiki is linked on group meeting recurring email)

---

# Meeting 2 - 8/10/20

## Pre-meeting notes:

### Things looked at this week:

- conda envs on wiay all set up (cloned important ones from root so i can add jupyter packages to them)

### Points I want to bring up:

- get chris to know my github repo

## Meeting minutes:

- Got a new primary Task (other than getting vit running) that is to get hunter's pre-trained box which outputs a set of paramters and generate a template using bibly to resample and get liklihoods then compare if this resampling imporvoves the original vit output!

  - more details: take the say 10,000 and use bilby to compute the liklihood of each point. Note bibly is a wrapper for nested sampling and MCMC techniques so defos has a function for calculating liklihood.
  - vit runs and gets say 10,000 samples of posterior.
  - categorical distibution

- vit changing prior:

  - once vit is run on a particular prior. can easily change to new prior without running again with a simple WEIGHT = NEW PRIOR / OLD PRIOR.

- vit desciption:

  - written in python files so just use vscode native python to run. This means we don't need to install any jupyter stuff and can use preset conda envs.
  - chris runs it in terminal with python scripts. He had to pip install with the --2020-version extension....will do that with a fresh venv justr on python, sounds good to me

- Report writing points:

  - INTRO: intro `grav waves` (it is still an astrophysics report after all) Intro `Machine Learning` in general maybe touch on parameter estimation and bayesian inference and old school techniques and new ML techniques and their improvements.
  - METHODOLOGY: Intro/decribe CVAE
  - RESULTS: cant take results ML and compare to MCMC or Nested as the old school takes weeks to run so it's tedious for sure!
  - TECHNICAL LEVEL: not too high as it might not be an expert marking it.

- literature work:
  - Shultz? Grav wave living reviews
    Catalog 01 02 (11 detections from the two runs combined) GWTCL

## Post-meeting tasks:

- find out what a CVAE is (seems VERY IMPORTANT)
- try install vit with venv and pip specifal in native python
- learn bilby
- focus more on literature - soure the 3 papers chirs mentioned above plus a newer review and another one that is one step before public access!
- research algorithm/framework of nested smapling (use w/ bilby)
- set up proper to-do system to start shifting away from handwritten notes.
- start daily jounral etc or maybe a week per file to easily search for weekly tasks type of thing

### Want to achieve for next week:

- have a overleaf template and add chris as colab on project
- have vit running on cpu (locally and on wiay)
  - go through side-by-side with vit paper and see what every line is doing (time consuming)
- found a nice jupyter notebook pipeline manager (like elyta+kubeflow) for vscode
- nice vscode env for ML on
- read and write up all papers i have currently in onedrive (~10)
- have made my mind up with webspace either using git submodules or not
- a significant amount of tf and torch practise

## Questions for next meeting:

---
