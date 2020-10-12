# ISSUE 1 - `VIT` INSTALL FAILS W/O `NUMPY`

## ISSUE DATE:

7/10/2020

## ISSUE WORKSPACE ENV:

Working Locally on CPU and `conda` python=3.6.12

## ISSUE DESC:

On a clean `conda` install, once we have `pip install --upgrade pip` then `pip install vitamin-b` it seems to fail on `line 20` of `requirements.txt` this is the line where `cpnest` is dealt with. It appears to install this package it needs to install `numpy` (before `numpy` itself is installed by iterating through `requirements.txt`) as seen on `line 184` of `issue1_failed_vit_install_no_numpy_terminal_ouput_log.txt`.

## ISSUE RESOLVE STEPS:

1. Will try `pip install numpy==1.18.4` (specific version from `requirements.txt`) on a clean `conda` env then `pip install vitamin-b`
2. might also be a `conda` issue so if RESOLVE STEP 1 doesn't work will try using `python -m venv` command instead (can do easily cause I'm local - if this works means we need a python3.6 interpreter on wiay (`conda` not usable))

## ISSUE RESOLVE STATUS:

Not sent to Hunter Yet

---

# ISSUE 2 - `VIT` FAILS WITH `NUMPY` AT BUILDING `CPNEST`

## ISSUE DATE:

7/10/20

## ISSUE WORKSPACE ENV:

Working Locally on CPU and `conda` python=3.6.12

## ISSUE DESC:

On clean `conda` env, `pip install numpy==1.18.4` first (as suggested in possible `ISSUE 1 RESOLVE`) then `pip install vitamin_b`. There seems to be a problem with building wheel for `cpnest` which is suspicious as it's the same package at the heart of `ISSUE 1`. Despite `pip` offering a short-term solution it seems `cpnest` isn's built completely properly (if it is built, it is by a counter-intuitive way that will become depreciated in later updates of `pip`). This is in excess of 4 `tensorflow` incompatibilities with different package versions. See `issue2_failed_vit_install_terminal_outputlog.txt` for details:

- `line 409-439` - failed to build wheel for `cpnest`
- `line 477-478` - confirms only `cpnest` package failed to build
- `line 480-482` - short-term solution that installs `cpnest` from legacy `setup.py` but this wont be possible in newer versions of `pip`
- `line 484` - gives solution for later `pip` updates how to keep the short-term fix working
- `line 486-489` - shows tensorflow incompatibilties with other packages

## ISSUE RESOLVE STEPS:

1. Compatibility issues I have a suspicion `conda` could be the problem. Specifically, mixing its installs with `pip`. Will try with `python -m venv` locally so I can use `pip` exclusively. If works, will be harder to run on wiay as is.
2. If `python -m venv` doesn't work could try installing `vit` from source (without the option `geos` and skymap stuff initially)

## ISSUE RESOLVE STATUS:

Not sent to Hunter yet

---

# ISSUE 3 - SAME AS `ISSUE 1&2` WITH `VIRUALENV` (NOT A `CONDA` PROBLEM - GOOD FOR WIAY)

## ISSUE DATE:

7/10/20

## ISSUE WORKSPACE ENV:

`virtualenv` locally on CPU python=3.6.9

## ISSUE DESC:

Firstly, same as `ISSUE 1` where `numpy` needs to be installed before `vit`. This time only `pip` was used so can confirm it's not a `conda` problem which makes working on wiay that much easier (once this issue is resolved). See file `issue3_failed_vit_install_with_virtualenv_cpnest_nobuild_terminal_ouput_log.txt` where `line 53` shows same error as `ISSUE 1` and `line60` shows me installing the right version of `numpy` manually.

Second part of issue is similar to `ISSUE 2` where `vit` install fails at building `cpnest` however this time there is a different error ouput log. I believe this is because I upgraded `pip` to `pip 20.2.3` so there isn't the same backup building from legacy setup.py as before in `ISSUE 2`. Initial build fail of `cpnest` occurs at `line 277-310`. But then after it doesn't try back up method and just fails at the `cpnest/paramter` stuff and exits.

## ISSUE RESOLVE STEPS:

1. Now that I have concluded it's not a `conda` problem can safely go back to using it. Will try next building from source by cloning the `vit` repo and using `virtualenv` as in the docs.
2. Despite errors, will try running the inital `vit` imports to see if it is working. Note, thi means I'll need to install `jupyter notebook` onto my `virtualenv` ontop of the packages from `requirements.txt` to get a local jupyter server up. Hope this doesn't mess with any dependencies etc...

## ISSUE RESOLVE STATUS:

Not sent to Hunter yet

---
