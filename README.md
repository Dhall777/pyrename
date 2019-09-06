# PythonFileRenaming
Bare bones program for file renaming.
I used this often in college; no more renaming bs files in my down time!

# Source code

import os
# Replace below with path containing targeted data
os.chdir(r'path_of_your_data_here')

for file in os.listdir():
    file_name, file_ext = (os.path.splitext(file))
    file_title, file_version = (file_name.split('-'))
    file_version = file_version.strip()
    file_ext = file_ext.strip()
    file_title = file_title.strip()
    new_name = '{}-{}{}'.format(file_version, file_title, file_ext)
    os.rename(file, new_name)
