# SSH

## Define SSH settings in config file:
Add the following lines in the under `~/.ssh/config` file
```
Host my-host-alias
    HostName 192.168.224.85
    User root
    IdentityFile C:/Users/username/.ssh/web-server.pem
```
Command to SSH the server: `ssh my-host-alias`
