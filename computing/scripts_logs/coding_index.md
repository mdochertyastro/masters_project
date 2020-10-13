# Overview

This is a one-stop-shop for all coding snippets, ideas and research (trying to replace the handwritten _computing manual_ I originally had) Note, there will be some intrinsic overlap between console and bash scripting but hopefully using ToC keeps it easy to keep track of. Python will probs have the biggest section by the end so might rethink structure if/when

---

## Topics I currrently have notes on:

### 1. Console

- find
- test
- chmod

### 2. Bash scripting

- variables

### 3. Python

### 4. Git

### 5. Conda

### 6. VS Code

---

## Things I want to research:

### 1. Console

- [ ] grep
- [ ] wget
- [ ] pipes
- [ ] echo (with variables) - make console ouput into a variable
- [ ] extracting some lines from a big output to print
- [ ] echo (print and into lines of files) (quotes or nah?)
- [ ] regEx
- [ ] cat

### 2. Bash scripting

- [x] variables
- [ ] header
- [ ] functions
- [ ] PATH

### 3. Python

- [ ] dictionaries
- [ ] numpy records
- [ ] class inheritance, methods and atributes and the self thingy
- [ ] package releases
- [ ] numpy stack

### 4. Git

- [ ] branching
- [ ] forking
- [ ] submodules
- [ ] remotes
- [ ] pull/push
- [ ] fetch

### 5. Conda

- setting 'which conda' as env variable
- cloning envs
- conda config work (syncs with .condarc)
-

### 6. VS Code

---

# 1. Console

## find

Only print stuff that's not 'permission denied'

```console
find <paths> ! -readable -prune -o <other conditions like -name> -print
```

---

## test

Gives info for all the conditional if statements like if dir exists do this (see goliath bashrc for usage)

```console
 man test
```

---

## chmod

chmod = 'change mode'
Have three options:

1. numerical changes
2. written changes
3. other random shortcuts

### Numerical changes

3 numbers represent permissions for different user-types. First is the owener, second is group and third is public. Numerical vals:

- 0 no permissions
- 1 can excecute (x)
- 2 can write (w)
- 4 can read (r)

Note we add these up for each user-type so:

- 7 = rwx
- 6 = rw
- 5 = rx
- 3 = wx

examples

```console
chmod 777 $file/dir # owner,group.public(rwx)
chmod 751 $file/dir # owner(rwx), group(rx), public(x)
```

### Written changes

This is more intuitive but less flexible as any changes apply to all user-types

```console
chmod +x $file/dir # adds x priv to all user-groups so if it was previously 444 it's now 555
chmod -x $file/dir # the minus removes priveleges to all user-types
```

### Random shortcuts

```console
chmod a=r $file/dir # sets read-only to all user-types
```

---

# 2. Bash scripting

## Variables

two types of variables:

1. global system variables
2. local user-defined variables

### 1. global

These are built-in to bash so can't be assigned but can be called using **brackets**

```console
matthew@goliath:~$ echo $(pwd)
/home/matthew
```

### 2. local

Local variables can be assigned to numerical values, strings, global variables or filepaths (probs more but these seem the common ones) (using brackets as above) and then called using \$ without brackets

**Local from global:**

```console
matthew@goliath:~$ conda_dir=$(which conda) # global assigned to local
matthew@goliath:~$ echo $conda_dir          # local called with echo
/home/matthew/anaconda3/condabin/conda
```

**Local from string/number:**

```console
matthew@goliath:~$ str='hello'
matthew@goliath:~$ echo $str
hello

matthew@goliath:~$ num=5
matthew@goliath:~$ echo $num
5
```

**Local from filepath:**

this is so far the most common type of variable I am setting in scripts. Don't need to set it as a string and can use it without brackets for commands:

```console
matthew@goliath:~$ dir=~/Desktop
matthew@goliath:~$ echo $dir
/home/matthew/Desktop

matthew@goliath:~$ ls $dir
home_test  python_interpreter  vitamin_local
```

---

# 3. Python

---

# 4. Git

- git pull = git fetch + git merge

---

# 5. Conda

---

# 6. VS Code
