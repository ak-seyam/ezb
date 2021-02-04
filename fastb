#!/usr/bin/env python

import sys
import os
import subprocess

try:
    menu = sys.argv[1]
except IndexError:
    print("please add your menu as the first arg", file=sys.stderr)
    sys.exit(1)

working_directory = os.getcwd()

directories = working_directory.split('/')

echo = subprocess.Popen(["echo", "\n".join(directories[1:])],stdout=subprocess.PIPE)
menu_out = subprocess.Popen([menu],stdin=echo.stdout, stdout=subprocess.PIPE)
output = menu_out.communicate()[0].decode('ascii')[:-1]

starting_index = working_directory.find("/"+output)
chosen_dir = working_directory[:starting_index+len(output)+1]

print(chosen_dir)
