# SSH

## Define SSH settings in config file:
Add the following lines in the under `~/.ssh/config` file
```
Host my-host-alias
    HostName remote.server.address (e.g. 192.168.0.1)
    User username
    IdentityFile C:/Users/username/.ssh/web-server.pem
```
Command to SSH the server: `ssh my-host-alias`

## Map a service to local machine via Jumpbox
```
ssh -L 3306:service.domain.com:3306 -i aws-keys/id_rsa user@jumpbox.address -N
```

## Cop a file from a remote server to local
`scp server-host:/var/log/tomcat/access.log C:/Temp`
