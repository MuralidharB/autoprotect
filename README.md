# Introduction
This python script can be registered as a cron job that runs under nova user on a TVM. The python script, when invoked, iterates through the domains and projects and discovers any instances that TVM did not yet protect. It creates a workload for each unprotected instance, so the instances are backed up at the specified interval.

# Usage
```
(myansible) [stack@tvm-1 ~]$ python autoprotect.py -h
usage: autoprotect.py [-h] rcfile

positional arguments:
  rcfile

optional arguments:
  -h, --help  show this help message and exit
  ```
  
  # Autoprotect configuration file
  The autoprotect.py requires a configuration file that includes information about the openstack cloud, users and their credentials. The complete listing is given here:
  ```
  ```
