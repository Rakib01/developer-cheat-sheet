A list of all Linux commands commonly used with Linux operating systems.
Linux Commands List

No matter whether you are new to Linux or an experienced user,
having a list of common commands close at hand is helpful.

- Navigate to HOME directory:

    ``` 
    cd or cd ~
    ```
- Move one level up:
    ```
    cd ..
    ```
- Displays the file content:
    ```
    cat filename
    ```
- Joins two files (file1, file2) and stores the output in a new file (file3):
    ```
    cat file1 file2 > file3
    ```
- Moves the files to the new location:
    ```
    mv file "new file path"
    ```
- Renames the file to a new filename":
    ```
    mv filename new_file_name
    ```


### Networking command

- login into a remote Linux machine using SSH:
    ```
    SSH username@ip-address or hostname
    ```
- To ping and Analyzing network and host connections:
    ```
    Ping hostname="" or =""
    ```
- Display files in the current directory of a remote computer:
    ```
    dir
    ```
- change directory to "dirname" on a remote computer:
    ```
    cd "dirname"
    ```
- 

### User management commands of linux

- To display value of a variable:
    ```
    sudo adduser username	
    ```
- Displays all environment variables:
    ```
    sudo passwd -l 'username'
    ```
- Create a new variable:
    ```
    sudo userdel -r 'username'	
    ```
- Remove a variable:
    ```
    sudo usermod -a -G GROUPNAME USERNAME
    ```
- To set value of an environment variable:
    ```
    sudo deluser USER GROUPNAME
    ```
