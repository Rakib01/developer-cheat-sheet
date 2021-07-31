### SYSTEM INFORMATION
- Display Linux system information
    ```
    uname -a
    ```

- Display kernel release information
    ```
    uname -r
    ```

- Show which version of Red Hat installed
    ```
    cat /etc/redhat-release
    ```

- Show how long the system has been running + load
    ```
    uptime
    ```

- Show system host name
    ```
    hostname
    ```

- Display all local IP addresses of the host.
    ```
    hostname -I
    ```

- Show system reboot history
    ```
    last reboot
    ```

- Show the current date and time
    ```
    date
    ```

- Show this month's calendar
    ```
    cal
    ```

- Display who is online
    ```
    w
    ```

- Who you are logged in as
    ```
    whoami
    ```
### HARDWARE INFORMATION
- Display messages in kernel ring buffer
    ```
    dmesg
    ```

- Display CPU information
    ```
    cat /proc/cpuinfo
    ```

- Display memory information
    ```
    cat /proc/meminfo
    ```

- Display free and used memory ( -h for human readable, -m for MB, -g for GB.)
    ```
    free -h
    ```

- Display PCI devices
    ```
    lspci -tv
    ```


### FILE PERMISSIONS
Linux chmod example
        PERMISSION      EXAMPLE

         U   G   W
        rwx rwx rwx     chmod 777 filename
        rwx rwx r-x     chmod 775 filename
        rwx r-x r-x     chmod 755 filename
        rw- rw- r--     chmod 664 filename
        rw- r-- r--     chmod 644 filename

- NOTE: Use 777 sparingly!

        LEGEND
        U = User
        G = Group
        W = World

        r = Read
        w = write
        x = execute
        - = no access

### NETWORKING
- Display all network interfaces and IP address
    ```
    ip a
    ```

- Display eth0 address and details
    ```
    ip addr show dev eth0
    ```

- Query or control network driver and hardware settings
    ```
    ethtool eth0
    ```

- Send ICMP echo request to host
    ```
    ping host
    ```

- Display whois information for domain
    ```
    whois domain
    ```

- Display DNS information for domain
    ```
    dig domain
    ```

- Reverse lookup of IP_ADDRESS
    ```
    dig -x IP_ADDRESS
    ```

- Display DNS IP address for domain
    ```
    host domain
    ```

- Display the network address of the host name.
    ```
    hostname -i
    ```

- Display all local IP addresses of the host.
    ```
    hostname -I
    ```

- Download http://domain.com/file
    ```
    wget http://domain.com/file
    ```

- Display listening tcp and udp ports and corresponding programs
    ```
    netstat -nutlp
    ```
### ARCHIVES (TAR FILES)
- Create tar named archive.tar containing directory.
    ```
    tar cf archive.tar directory
    ```

- Extract the contents from archive.tar.
    ```
    tar xf archive.tar
    ```

- Create a gzip compressed tar file name archive.tar.gz.
    ```
    tar czf archive.tar.gz directory
    ```

- Extract a gzip compressed tar file.
    ```
    tar xzf archive.tar.gz
    ```

- Create a tar file with bzip2 compression
    ```
    tar cjf archive.tar.bz2 directory
    ```

- Extract a bzip2 compressed tar file.
    ```
    tar xjf archive.tar.bz2
    ```

### SSH LOGINS
- Connect to host as your local username.
    ```
    ssh host
    ```

- Connect to host as user
    ```
    ssh user@host
    ```

- Connect to host using port
    ```
    ssh -p port user@host
    ```
### FILE TRANSFERS
- Secure copy file.txt to the /tmp folder on server
    ```
    scp file.txt server:/tmp
    ```

- Copy *.html files from server to the local /tmp folder.
    ```
    scp server:/var/www/*.html /tmp
    ```

- Copy all files and directories recursively from server to the current system's /tmp folder.
    ```
    scp -r server:/var/www /tmp
    ```

- Synchronize /home to /backups/home
    ```
    rsync -a /home /backups/
    ```

- Synchronize files/directories between the local and remote system with compression enabled
    ```
    rsync -avz /home server:/backups/
    ```
### DISK USAGE
- Show free and used space on mounted filesystems
    ```
    df -h
    ```

- Show free and used inodes on mounted filesystems
    ```
    df -i
    ```

- Display disks partitions sizes and types
    ```
    fdisk -l
    ```

- Display disk usage for all files and directories in human readable format
    ```
    du -ah
    ```

- Display total disk usage off the current directory
    ```
    du -sh
    ```

- Go to the $HOME directory
    ```
    cd
    ```

- Change to the /etc directory
    ```
    cd /etc
    ```