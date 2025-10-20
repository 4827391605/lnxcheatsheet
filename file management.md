### 2025-10-16
ls
lists files in the current directory

ls- l
long listing style i.e. (owner, size, allowed actions)

ls -a
 shows hidden files that start with .

ls -lh
 human readable sizes

tree
view directory tree

Navigation

cd /path/to/dir changes to a directory

cd .. go up in one directory

cd - go to home directory

pwd print currect directory

Creating files

touch file.txt create new empty file

mkdir new_folder create a new directory

mkdir -p parent/child create nested directories

Copying files and directories

cp file1.txt file2.txt copy file

cp -r dir1/ dir2/ copy directory recursively

cp -i file1.txt backup.txt prompting before overwrite

Moving and renaming

mv file.txt /new/location/ moves file to new location

mv oldname.txt newname.txt renames file

mv -i file.txt /new/location/ another way to prompt before overwrite

Deleting Files and Directories

rm file.txt abomination of the file

rm -i file.txt proceeding to delete/confirmation

rm -r folder/ recursively deletes directory

rm -rf folder/ force delete without prompt

Finding files

find . -name "*.log" find all of the log files

find /path/to/search -type f -size +1M find files over 1MB in/var/log

find /path/to/search -type f -mmin -10 find files modified less than 10 minutes ago

find /path/to/search -type f -mtime -1 find files modified within yesterday up till the moment

find /path/to/search -type d find directories instead of files
