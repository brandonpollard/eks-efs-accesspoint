# Example of using an access point.

*Using an access point:*

In the pod:  
  
[root@bpollard-app /]# ls -l /  
total 4  
lrwxrwxrwx   1 root root    7 Nov  3 15:22 bin -> usr/bin  
drwxr-xr-x   2 root root 6144 Feb 11 17:37 data  
drwxr-xr-x   5 root root  360 Feb 11 17:40 dev  
drwxr-xr-x   1 root root   66 Feb 11 17:39 etc  
drwxr-xr-x   2 root root    6 Nov  3 15:22 home  
... truncted ...  
  
[root@bpollard-app /]# cat /data/info.txt  
inside of the access point  
  
  
*Without an access point:*

  
[root@bpollard-app /]# ls -l /data/  
total 8  
drwxr-xr-x 2 root root 6144 Feb 11 20:04 data00  
-rw-r--r-- 1 root root   10 Feb 11 17:29 info.txt  
[root@bpollard-app /]# ls -lR /data/  
/data/:  
total 8  
drwxr-xr-x 2 root root 6144 Feb 11 20:04 data00  
-rw-r--r-- 1 root root   10 Feb 11 17:29 info.txt  
  
/data/data00:  
total 4  
-rw-r--r-- 1 root root 27 Feb 11 20:04 info.txt  
  
  
*Not* specifying an accesspoint in the configuration and only the EFS ID we can see all the files that have been created on the EFS filsystem.

Only the EFS filesystem  
volumeHandle: fs-f5249601  
  
EFS and access point  
volumeHandle: fs-f5249601::fsap-0a7ea0fbf2a9ebf6a  