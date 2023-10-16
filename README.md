Logrotate is prone to a race condition after renaming the logfile.
If logrotate is executed as root, with option that creates a file ( like create, copy, compress, etc.) and the user is in control of the logfile path, it is possible to abuse a race-condition to write files in ANY directories. 
An attacker could elevate his privileges by writing reverse-shells into directories "/etc/bash_completition.d/".
https://github.com/whotwagner/logrotten/blob/master/README.md
