# ezb. easy back in your terminal
back directories menu maker for dmenu like software, the following example uses pmenu but any dmenu-like alternative should work
## Demo
![ezb_demo](https://raw.githubusercontent.com/A-Siam/ez-b/main/demo.gif?token=AIKY2B3EXIEZTT64DAPTGWTAEV7LO)
## Setup
Assuming that enviromnet variable called `$SCRIPTS_DIR` points to a directory with ezb script in it. You can for sure save it to any directory you want.

1- create a file to be sourced for example
```bash
cd /any/path/you/want
echo "cd $($SCRIPTS_DIR/ezb $1)" > ezb_ # this is the ezb_ example file
```
2- add the following to your bash/zsh.rc
```bash
alias ezb="source /any/path/you/want/ezb_ $MENU" # on my system $MENU is pmenu but it can be any alternative
```
