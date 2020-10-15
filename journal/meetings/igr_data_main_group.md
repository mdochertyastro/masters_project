# Outline: IGR-data Group Meetings

Hour meeting fortnightly on Tuesday afternoon, usually ~20 people go round 1 by 1 and have 2 minute presentation on everything theyve been working on over past two weeks. Sometimes at the end there is a more deep presentation by a speaker. This is the breadth of awareness for igr-data group that compliments the depth of the igr-data ML club meetings.

# Meeting 1 - Tuesday 29/9/20

---

- ~10 peeps at first meeting with dan and prof heng, looks like it's chaired by chirs which is exciting

- staarted by going round one by one and telling the group what we have done over the past week

- using ML to speed up selection function compared to using monte carlo stuff

- extended GLADE catalogue with Martin Hendry

# Meeting 2 - Tuesday 6/10/20

- 14:12:33 From John Veitch : conda install python=3.6.0
  14:14:03 From Daniel Williams : Alternatively, if you can't use conda I think we have pyenv on Wiay which will let you use whichever python version you need.
  14:14:19 From John Veitch : conda is available for everyone I believe
  14:14:26 From Michael Williams : yeah, pretty sure it is
  14:14:28 From Hunter Gabbard : Ah haven’t used peenv
  14:14:48 From Hunter Gabbard : As long as conda is available, John’s suggestions should probably work
  14:15:15 From Hunter Gabbard : Assuming, there’s no weird sudo privilege things
  14:15:17 From Daniel Williams : Conda is probably he simplest way to do this (much as I'll groan about it)
  14:15:18 From John Veitch : conda create -n py36 python=3.6
  14:15:27 From John Veitch : Created a conda env for me with python3.6
  14:15:34 From Hunter Gabbard : Nice. Yeah do that then
  14:15:55 From Michael Williams : It can also do more recent versions (I'm using 3.8)
  14:16:04 From Matthew Docherty : I used miniconda from hercules over summer. Is there somewhere simlar in wiay I can add to my .bashrc so i can use conda in wiay. As currently 'conda' is not recognsied
  14:16:20 From Daniel Williams : Oh; that's a bit odd
  14:17:08 From Matthew Docherty : when i do 'conda --help' it's 'conda: command not found'
  14:17:21 From Daniel Williams : I'll just have a look at how it's set up
  14:17:31 From John Veitch : The full path is /usr/local/conda/bin/conda but it ought to be in your \$PATH
  14:17:44 From Daniel Williams : What's your username Matthew?
  14:17:48 From Matthew Docherty : 2259886d
  14:18:02 From Daniel Williams : Ahh
  14:18:19 From Daniel Williams : It's probably a bad setting in your .bashrc file, if you copied that over from the solar system.
  14:18:46 From Daniel Williams : If you try commenting out the bits in the section you've titled `### MY SCRATCH MINICONDA CONFIG' I think it should work.
  14:18:59 From Matthew Docherty : awesome will try that now
  14:19:16 From Daniel Williams : You'll need to logout and back in afterwards
  14:19:40 From Michael Williams : Also have a look at .condarc, you'll want to make sure it has the correct paths to your environments
  14:20:16 From Daniel Williams : I think that's fine, since conda's never run
  14:20:37 From Daniel Williams : (you don't have a .condarc file yet on the IGR system)

- now have conda working on wiay and can add my own env and specify it into my scratch where I have write priveleges!
- then now I have training data in my scratch will try tonight
- need to get jupyterlab working on wiay with nice aliases (make a funct6ion that takes host name as conditional argument to shoot to different webspaces)
- write up meeting 1 tonight with chris

- try using tf and torch learn both at same time and use them side by side

- Had a 20minute talk from Akshara Viswanathan. She has just finsihed her Masters PGT with chris and now started phd in netherlands. It's on Grav lensing from binary BBH mergers
  - She used bilby to create corner plots
  - want to get her github link to project

# Meeting 3 - Tuesday 13/10/20

Attendance - 21 people

## Notes for 2 minute pres:

- Created global repo that has 2 submodules in it
- started compiling BibTeX of all myt collated articles

## Pres:

### Jo Bayley

- parameter estimation using ML not MCMC
- SOAP data search output now arting on a paper, [old school method paper](https://arxiv.org/abs/1903.12614)

### Hunter

- waiting for old school sampling to run
- using CVAE for param estimation
- importance sampling - interesting technique that re-weights stuff after-the-fact
  - re-sampling to get a different wavefront
- working on making code applicable to REAL noise and signals not just pretty gaussian.

### Jordan McGinn

- Neutron star EOS new project
- needs CVAE for project so will speak to Crhis and Hunter
- he will be using CVAE to param estimate, he doesn't know which params yet but knows he wants grav mass and deformability
- inputs defomrabiblty params from a prev run then processes this to get EOS ouput

### Nicola De Lillo

- Working with JOh nand Graham param est for Pulsars

### Jetrho Linley

- multiband data analysis
- he is getting posteriors for 3 years of LISA signals, testing them is the newxt stage to make sure they are reliable postseriors using subsampling etc
- he has been simulating LISA noise for past 8 months and has sourced the LISA noise via code from an [official source](https://arxiv.org/abs/1803.01944)
- working in time domain, getting signal from the majiory book
- making own noise from noise curve
  all only in the time domain
- doing some 'PE' runs - **look up what this is**
- speeding up code by using fischer matrix to speed up priors in bilby

  - fischer were taking ages but he sped it up changing it from double-sided to single-sided factorisation
  - uses all wiay CPU for about 5mins (1min per param derivative for a 3 year signal)

- SNR approx function that approxs it fast
- working out how to test code

### Christian C... Bird

- applying jo's SOAP python module to diff GW sources to do with LISA
- jo's code currently finds signletracks then subtract somthing from that iteratively to create diff tracks to get multiple source identification
- got it off gitlab and added some 'minor issues'

### federico

- GW cosmo for para estimation of hubble constant
- found a paper masters student from berkely that used GW190814 to estimate H_0

### Leigh Smith

- reading papers about hyperbolic and parabolic encounters
- working with Zurich with coherent wave burst stuff
- continuing work thats Daniel's being doing with Zurich
- she will be learning how to run CWDB13? think its a code i nZurich rather than just using the output she will actually be running

### Rachel Gray

- fixed a bug in GW cosmo (so GW cosmo is a code package?)
- looking for another bug that is causing it to not work properly
- found more recent bug in the way mass priors are being defined but only for the latest release so not too serious a problem
- it uses bibly to get priors
- best place to get informed is the [bilby slack](https://join.slack.com/t/bilby-code/shared_invite/zt-a6znzsjl-EHHmtIIE5p__tu9JfLzrzw) in general (Rachel is getting invited to the slack now)

### Michael Williams

- working on paper draft comments
- unexpected results when running something that shouldnt run as inputs are too high but it still runs so will look into it

### Heni

- update to LISA code called LISA node to make LISA noise

### me

john veitch wrote cpnest, the pip version is january of this year

https://github.com/johnveitch/cpnest/commit/9087bd5fafe4479fb2bd792eb723341e600e490d
https://github.com/johnveitch/cpnest/commit/7352253d89ebb87caea653b1370ac2e94f781dd2

These are the commits that MIchael made to cpnest that make4s it work BUT they are not the version on pip

### Joe Perry

- using ML to reconstruct mass dynamics of modelled burst signals
- just been reading ML GW papers
- started playing around with PYtorch CVAE example
- Jo Bayley has a nice CVAE in PyTorch (he will send to Joe and Heni

### Reem 