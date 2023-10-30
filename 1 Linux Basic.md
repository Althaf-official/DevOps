# How many directories and files are present in /home/thor/test_dir directory?

Run: `tree /home/thor/test_dir` command and count the number of files and directories

# Which text file is not present under /home/thor/test_dir/ directory?

Run: ls /home/thor/test_dir/*.txt to check all text files under /home/thor/test_dir/ directory.

# Create an empty file inside /home/thor/ directory.


file name : empty_file.txt

Run touch /home/thor/empty_file.txt

# Create file with content inside /home/thor/ directory.


file name : contents_file.txt

content : This is not empty file

With help of echo command, redirect the content into a file.

Run: echo "This is not empty file" > /home/thor/contents_file.txt


# Create an empty directory inside /home/thor/ directory.

directory name : empty_dir

Run: mkdir /home/thor/empty_dir


# Create directory hierarchy inside /home/thor/ directory.


directory hierarchy: /home/thor/asia/india/bangalore


Run: mkdir -p /home/thor/asia/india/bangalore


# Copy target file to target directory


target file name : /home/thor/asia/bangalore.txt

target directory : /home/thor/asia/india/bangalore

`cp -v /home/thor/asia/bangalore.txt /home/thor/asia/india/bangalore`


# Copy source directory to target location


source directory name : /home/thor/asia/india/bangalore

target location: /home/thor/


Run: cp -r /home/thor/asia/india/bangalore /home/thor/


# Remove target file from target directory


target file name : bangalore.txt

target directory : /home/thor/asia/

Run: rm /home/thor/asia/bangalore.txt


#  Remove target directory and its contents.


target directory : /home/thor/asia/india/bangalore


Run: rm -r /home/thor/asia/india/bangalore









