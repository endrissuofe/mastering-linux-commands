# Linux Commands Deep Dive

This document captures my hands-on learning experience with Linux commands in the DevOps program. Each command is shown with practical examples followed by a screenshot of its terminal output.

---

## 1. What is a Linux Command?

A Linux command is a typed instruction executed in the terminal.

**Syntax:**  
`command [option] [argument]`

Example:  
```bash
ls -l /home
```

![ls -l /home screenshot](screenshots/ls-home.png)

---

## 2. Manipulating Files and Directories

### 2.1 `sudo`

Grants superuser privileges.

Command to create a folder without `sudo`:
```bash
mkdir /root/example
```
_Result: Permission denied_  
  
![mkdir /root/example permission denied](screenshots/Pernission%20denied.png)

Now with `sudo`:
```bash
sudo mkdir /root/example
```
_Result: Success_  
  
![sudo mkdir /root/example screenshot](screenshots/sudo_mkdir_success.png)

Finally, to verify:
```bash
sudo ls -l /root
```
  
![sudo ls -l /root screenshot](screenshots/verify_folder_created.png)

---

### 2.2 `pwd`

Show current working directory.

```bash
pwd
```

![pwd output screenshot](screenshots/pwd_output.png)

---

### 2.3 Linux Directory Structure

Change directory to root and list contents:
```bash
cd /
```

![cd / screenshot](screenshots/cd_root.png)

List the root directory:
```bash
ls
```
 
![ls / screenshot](screenshots/cd_root.png)

Change directory to `/usr`:
```bash
cd /usr
```
 
![cd /usr screenshot](screenshots/cd_usr.png)

And list contents there:
```bash
ls
```
 
![ls /usr screenshot](screenshots/ls_usr.png)

---

### 2.4 `cd`

Change to a specific directory, then show the working directory:
```bash
cd /usr/photos
```
 
![cd /usr/photos screenshot](screenshots/cd_photos.png)

```bash
pwd
```

![pwd in /usr/photos screenshot](screenshots/pwd_photos.png)

---

### 2.5 Side Hustle Task 1

1. Create a directory in `/usr`:
    ```bash
    sudo mkdir /usr/photos
    ```
    
    ![sudo mkdir /usr/photos screenshot](screenshots/cd_photos.png)

2. Change into the new directory:
    ```bash
    cd /usr/photos
    ```
   
    ![cd /usr/photos screenshot](screenshots/cd_photos.png)

3. Create three subdirectories:
    ```bash
    sudo mkdir dir1 dir2 dir3
    ```
    
    ![mkdir subdirectories screenshot](screenshots/mkdir_subdirs.png)

4. List the directories:
    ```bash
    ls -l
    ```
    ![ls -l /usr/photos screenshot](screenshots/ls_photos.png)

5. Change into one of them:
    ```bash
    cd dir1
    ```
    ![cd dir1 screenshot](screenshots/cd_dir1.png)

6. Confirm current directory:
    ```bash
    pwd
    ```
 
    ![pwd in dir1 screenshot](screenshots/pwd_dir1.png)

---

### 2.6 `ls`

List files with various options:

1. Basic listing:
    ```bash
    ls
    ```
    ![ls screenshot](screenshots/ls.png)

2. Long listing format:
    ```bash
    ls -l
    ```
    ![ls -l screenshot](screenshots/ls_l.png)

3. Including hidden files:
    ```bash
    ls -a
    ```
    ![ls -a screenshot](screenshots/ls_a.png)

4. Recursive listing with human-readable sizes:
    ```bash
    ls -lhR /home
    ```
    _Screenshot:_  
    ![ls -lhR /home screenshot](screenshots/ls_lhR_home.png)

---

### 2.7 `cat`

Display file contents:

```bash
cat /etc/os-release
```
 
![cat /etc/os-release screenshot](screenshots/cat_osrelease.png)

---

### 2.8 `cp`

Copy files and directories.

1. Copy a file:
    ```bash
    cp filename.txt /home/ubuntu/Documents
    ```
    
    ![cp file screenshot](screenshots/cp_file.png)

2. Copy multiple files:
    ```bash
    cp file1.txt file2.txt /home/ubuntu/Documents
    ```
    
    ![cp multiple files screenshot](screenshots/cp_multiple_files.png)

3. Copy a file to a new name:
    ```bash
    cp source.txt destination.txt
    ```
      
    ![cp rename screenshot](screenshots/cp_rename.png)

4. Recursively copy a directory:
    ```bash
    cp -R source_dir/ destination_dir/
    ```
     
    ![cp directory screenshot](screenshots/cp_directory.png)

---

### 2.9 `mv`

Move or rename files.

1. Move a file:
    ```bash
    mv filename.txt /home/ubuntu/Documents
    ```
     
    ![mv file screenshot](screenshots/mv_file.png)

2. Rename a file:
    ```bash
    mv oldname.txt newname.txt
    ```
   
    ![rename file screenshot](screenshots/mv_rename.png)

---

### 2.10 `rm`

Delete files or directories.

1. Remove a file:
    ```bash
    rm file.txt
    ```
      
    ![rm file screenshot](screenshots/rm_file.png)

2. Remove multiple files:
    ```bash
    rm file1.txt file2.txt
    ```
 
    ![rm multiple files screenshot](screenshots/rm_multiple_files.png)

3. Remove a directory recursively:
    ```bash
    rm -rf folder_name/
    ```
    _Screenshot:_  
    ![rm folder screenshot](screenshots/rm_folder.png)

---

### 2.11 `touch`

Create an empty file.

```bash
touch /home/ubuntu/Documents/Web.html
```
  
![touch file screenshot](screenshots/touch_web_html.png)

---

### 2.12 `find`

Search for files by name.

```bash
find / -name "Web.html"
```
 
![find file screenshot](screenshots/find_web_html.png)
