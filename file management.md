### 2025-10-16

# File management — Cheatsheet
Date: 2025-10-16

## Listing files
- ls  
  lists files in the current directory

- ls -l  
  long listing (owner, size, permissions, timestamp)

- ls -a  
  shows hidden files (names starting with .)

- ls -lh  
  long listing with human-readable sizes

- tree  
  view directory tree (may require `sudo apt install tree`)

## Navigation
- cd /path/to/dir  
  change to a directory

- cd ..  
  go up one directory

- cd -  
  go to previous directory

- pwd  
  print current directory

## Creating files and directories
- touch file.txt  
  create a new empty file (or update timestamp)

- mkdir new_folder  
  create a new directory

- mkdir -p parent/child  
  create nested directories (parents as needed)

## Copying files and directories
- cp file1.txt file2.txt  
  copy file

- cp -r dir1/ dir2/  
  copy directory recursively

- cp -i file1.txt backup.txt  
  prompt before overwrite

## Moving and renaming
- mv file.txt /new/location/  
  move file to new location

- mv oldname.txt newname.txt  
  rename file

- mv -i file.txt /new/location/  
  prompt before overwrite

## Deleting files and directories
- rm file.txt  
  remove file

- rm -i file.txt  
  prompt before delete

- rm -r folder/  
  recursively delete directory

- rm -rf folder/  
  force delete without prompt (dangerous)

## Finding files
- find . -name "*.log"  
  find all .log files under current directory

- find /path/to/search -type f -size +1M  
  find files over 1MB

- find /path/to/search -type f -mmin -10  
  find files modified in the last 10 minutes

- find /path/to/search -type f -mtime -1  
  find files modified within the last 24 hours

- find /path/to/search -type d  
  find directories instead of files

## File permissions and ownership
Use `chmod` to change permissions and `chown` to change ownership.

- chmod +r file.txt  
  add read permission (for relevant class: u/g/o or all with +r)

- chmod -r file.txt  
  remove read permission

- chmod +w file.txt  
  add write permission

- chmod -w file.txt  
  remove write permission

- chmod +x script.sh  
  make file executable

- chmod u+r file.txt  
  owner read

- chmod g+w file.txt  
  group write

- chmod o-x script.sh  
  remove execute for others

Numeric mode examples:
- chmod 755 file.txt  
  owner rwx, group r-x, others r-x

Changing ownership:
- chown user:group file.txt  
  change owner and group

- chown -R user:group /path/to/dir  
  change ownership recursively

### Common numeric permission modes
- 777 — read/write/execute for owner, group, others  
- 755 — owner rwx, group r-x, others r-x  
- 700 — owner rwx, no permissions for group/others  
- 666 — read/write for owner, group, others  
- 644 — owner rw, group r, others r  
- 600 — owner rw, none for group/others  
- 555 — read & execute for all  
- 440 — read-only for owner/group, none for others  
- 400 — read-only for owner  
- 711 — owner rwx, group execute-only, others execute-only

## Archiving and compression
- tar -cvf archive.tar folder/  
  create an uncompressed archive

- tar -xvf archive.tar  
  extract archive

- tar -czvf archive.tar.gz folder/  
  create gzip-compressed archive

- tar -xzvf archive.tar.gz  
  extract gzip-compressed archive

---

Notes:
- Use code blocks when running commands in examples.  
- Be careful with destructive commands (`rm -rf`, `chmod 777`).  
- Consider adding examples for `rsync`, `scp`, and `zip/unzip` for completeness.