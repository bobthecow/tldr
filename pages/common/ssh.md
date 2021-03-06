# SSH

> Secure Shell is a protocol used to securely log onto remote systems.
> It can be used for logging or executing commands on a remote server.

- connecting to a remote server

`ssh {{username}}@{{remote_host}}`

- connecting to a remote server with specific port

`ssh {{username}}@{{remote_host}} -P {{2222}}`

- ssh tunneling: dynamic port forwarding (SOCKS proxy on localhost:9999) 

`ssh -D {{9999}} -C {{username}}@{{remote_host}}`

- ssh tunneling: forward a specific port (localhost:9999 to slashdot.org:80)

`ssh -L {{9999}}:slashdot.org:80 {{username}}@{{remote_host}}`
