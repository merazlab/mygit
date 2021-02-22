## SSH setup

[Ref link](https://www.e2enetworks.com/help/knowledge-base/set-up-ssh-keys/)

## 

Step 1 – Create the RSA Key Pair
```ssh-keygen -t rsa
```
Steo 2 - Set name  
```id_name
```
Step 3 – Copy the Public Key to your server node
Method-1
```
ssh-copy-id -i $HOME/.ssh/id_name.pub user@server1.cyberc
```
Method - 2
rsync -zaP 
