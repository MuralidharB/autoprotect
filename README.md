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
  The autoprotect.py requires a configuration file that includes information about the openstack cloud, users and their credentials. A sample configuration file `autoprotect.rc` is checked in as part of the repo. To keep the parsing logic simple, we expect each line of the parameter is expected to start with a keywork `export`. Any lines that do not start with this keyword is ignored by the python code.
