# Homework CI/CD in Github Actions

## Project settings
Set Java 8 into IDEA File/Project structure

Mark src/main/java  
Mark src/test/java  

##Add your repo into Actions secrets and variables  

- SERVER_IP: VDS IP for deploy
- SERVER_PATH: path to deploy on your VDS
- SERVER_USER: user in your VDS
- SSH_PRIVATE_KEY: private key.  

###Use commands for creation key on VDS (log in SERVER_USER):  
- ssh-keygen -t rsa -b 4096 -C "your_email@example.com"  
- cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys  
- cat ~/.ssh/id_rsa copy to SSH_PRIVATE_KEY (GitHub Action secret)  

####Create SERVER_PATH/stop.sh  
For example:  
``` 
#!/bin/bash
echo "Yeah! It's works!!! Hello from VDS"
```
Run chmod +x stop.sh