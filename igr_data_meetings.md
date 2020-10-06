# Meeting 1 - Tuesday 29/9/20
---

- ~10 peeps at first meeting with dan and prof heng, looks like it's chaired by chirs which is exciting

- staarted by going round one by one and telling the group what we have done over the past week

- using ML to speed up selection function compared to using monte carlo stuff

- extended GLADE catalogue with Martin Hendry 

# Meeting 2 - Tuesday 6/20/20
---

- 14:12:33	 From John Veitch : conda install python=3.6.0
14:14:03	 From Daniel Williams : Alternatively, if you can't use conda I think we have pyenv on Wiay which will let you use whichever python version you need.
14:14:19	 From John Veitch : conda is available for everyone I believe
14:14:26	 From Michael Williams : yeah, pretty sure it is
14:14:28	 From Hunter Gabbard : Ah haven’t used peenv
14:14:48	 From Hunter Gabbard : As long as conda is available, John’s suggestions should probably work
14:15:15	 From Hunter Gabbard : Assuming, there’s no weird sudo privilege things
14:15:17	 From Daniel Williams : Conda is probably he simplest way to do this (much as I'll groan about it)
14:15:18	 From John Veitch : conda create -n py36 python=3.6
14:15:27	 From John Veitch : Created a conda env for me with python3.6
14:15:34	 From Hunter Gabbard : Nice. Yeah do that then
14:15:55	 From Michael Williams : It can also do more recent versions (I'm using 3.8)
14:16:04	 From Matthew Docherty : I used miniconda from hercules over summer. Is there somewhere simlar in wiay I can add to my .bashrc so i can use conda in wiay. As currently 'conda' is not recognsied 
14:16:20	 From Daniel Williams : Oh; that's a bit odd
14:17:08	 From Matthew Docherty : when i do 'conda --help' it's 'conda: command not found'
14:17:21	 From Daniel Williams : I'll just have a look at how it's set up
14:17:31	 From John Veitch : The full path is /usr/local/conda/bin/conda but it ought to be in your $PATH
14:17:44	 From Daniel Williams : What's your username Matthew?
14:17:48	 From Matthew Docherty : 2259886d
14:18:02	 From Daniel Williams : Ahh
14:18:19	 From Daniel Williams : It's probably a bad setting in your .bashrc file, if you copied that over from the solar system.
14:18:46	 From Daniel Williams : If you try commenting out the bits in the section you've titled `### MY SCRATCH MINICONDA CONFIG' I think it should work.
14:18:59	 From Matthew Docherty : awesome will try that now
14:19:16	 From Daniel Williams : You'll need to logout and back in afterwards
14:19:40	 From Michael Williams : Also have a look at .condarc, you'll want to make sure it has the correct paths to your environments
14:20:16	 From Daniel Williams : I think that's fine, since conda's never run
14:20:37	 From Daniel Williams : (you don't have a .condarc file yet on the IGR system)

- now have conda working on wiay and can add my own env and specify it into my scratch where I have write priveleges!
- then now I have training data in my scratch will try tonight
- need to get jupyterlab working on wiay with nice aliases (make a funct6ion that takes host name as conditional argument to shoot to different webspaces)
 - write up meeting 1 tonight with chris 


 - try using tf and torch learn both at same time and use them side by side

 - Had a 20minute talk from Akshara Viswanathan. She has just finsihed her Masters PGT with chris and now started phd in netherlands. It's on Grav lensing from binary BBH mergers
    - She used bilby to create corner plots
    - want to get her github link to project