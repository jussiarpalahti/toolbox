
# Open Data Toolbox

## SSH tunnel for VNC connection

```
ssh -N -f -i ~/.ssh/ssh_private_key -L 5901:localhost:5901 user@remote.host
```

 * -N means no commands
 * -f means go to background
 * change identity key, remote username and host

## Convert SSH key to PEM key for Azure

```
openssl req -x509 -key ~/.ssh/private_key.rsa -nodes -days 365 -newkey rsa:2048 -out public_key.pem
```

In this example private key is in RSA format. Example came from SO post so I can't vouch for its security. For example only!