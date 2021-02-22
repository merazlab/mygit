## SSH setup

[Ref link](https://www.e2enetworks.com/help/knowledge-base/set-up-ssh-keys/)

## 
Step 0 - cerate .ssh hidden folder

```
cd  ~           #go to home directory

mkdir .ssh      #create folder

cd .ssh         #go inside .ssh directory

```

Step 1 – Create the RSA Key Pair

` ssh-keygen -t rsa `

Step 2 - Set name  

`id_name `

Step 3 – Copy the Public Key to your server node

Method-1

`ssh-copy-id -i $HOME/.ssh/id_name.pub user@server1.cyberc `

Method - 2

`
rsync -zaP  id_name.pub user@addres:
`

Step 4 - Server end setting

```
$ cd
$ mkdir .ssh && touch .ssh/authorized_keys
$ chmod 700 .ssh/ && chmod 600 .ssh/authorized_keys
$ cat id_name.pub >> .ssh/authorized_keys
```


---
## Additional setting for hide ip in host side

```
touch ~/.ssh/config #create file
```
Write inside file
`vi ~/.ssh/config `


```
Host javed
	User javed
	HostName 172.20.70.12
	IdentityFile ~/.ssh/ccf_javed

Host pawan
    User pawan
    HostName 172.20.70.12
    IdentityFile ~/.ssh/ccf_pawan
Host pro
    User pro2016001
    HostName 172.31.1.45
    IdentityFile ~/.ssh/pro
```