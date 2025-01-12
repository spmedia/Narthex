# Narthex
Narthex (Greek: Νάρθηξ, νάρθηκας) is a modular & minimal dictionary generator for Unix and Unix-like operating system written in C and Shell. It contains autonomous Unix-style programs for the creation of personalised dictionaries that can be used for password recovery & security assessment. The programs make use of Unix text streams for the collaboration with each other, according to the Unix philosophy. It is licensed under the GPL v3.0. Currently under development!

*I made a video to explain the usage of Narthex to non-Unix people:*
https://www.youtube.com/watch?v=U0UmCeLJSkk&t=938s
(the timestamp is intentional)

## The tools
+ nchance   -  A capitalization tool that appends the results to the bottom of the dictionary.
+ ninc      -  A incrementation tool that multiplies alphabetical lines and appends an n++ at the end of each line.
+ ncom      -  A combination tool that creates different combinations between the existing lines of the dictionary.
+ nrev      -  A reversing tool, that appends the reserved versions of the lines at the end of the dictionary.
+ nleet     -  A leetifier. Replaces characters with Leet equivalents, such as @ instead of a, or 3 instead of e.
+ nclean    -  A tool for removing passwords that don't meet your criteria (too short, no special characters etc.)
+ nwiz      -  A wizard that asks for the infromation and combines the tools together to create a final dictionary.

## Install
In order to install, execute the following commands:
```
$ git clone https://github.com/MichaelDim02/Narthex.git && cd Narthex
$ sudo make install
```

## Usage
For easy use, there is a wizard program, nwiz, that you can use. Just run
```
nwiz
```
And it will ask you for the target's information & generate the dictionary for you.

For advanced usage, you can read the manpages of each tool. What they all do, really, is enhance small dictionaries. For example you can run
```
cat words.txt | nhance -f | nrev | nleet | ninc 1 10 > words2.txt
```
on a small wordlist and you can see the result for yourself.
