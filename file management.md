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

File Permissions and Ownership

chmod +r file.txt lets all users to read the file

chmod -r file.txt prevents any user from reading the file

chmod +w file.txt allows all users to make changes to the file

chmod -w file.txt prevents any user from making changes to the file

chmod +x script.sh allows all users to execute the file

chmod u+r file.txt allows the owner to read the file

chmod u-r file.txt prevents the owner from reading the file

chmod u+w file.txt allows the owner to make changes to the file

chmod u-w file.txt prevents the owner from making changes to the file

chmod u+x script.sh allows the owner to execute the file

chmod u-x script.sh prevents the owner from executing the file

chmod g+r file.txt allows the group to read the file

chmod g-r file.txt prevent the group from reading the file

chmod g+w file.txt allows the group to make changes to the file

chmod g-w file.txt prevents the group from making changes to the file

chmod g+x script.sh allows the group to execute the file

chmod g-x script.sh prevents the group from executing the file

chmod o+r file.txt allows others to read the file

chmod o-r file.txt prevents others from reading the file

chmod o+w file.txt allows others to make changes to the file

chmod o-w file.txt prevent others from making changes to the file

chmod o+x script.sh allows others to execute the file

chmod o-x script.sh prevents others from executing the file

chmod 755 file.txt sets specific permissions (see table, below)

chown user:group file.txt changes ownership

chown -R user:group /path/to/dir changes ownership recursively (for directories)

