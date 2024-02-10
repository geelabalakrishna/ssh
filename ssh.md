# Configure SSH Key-Based Authentication on a Linux Server

- Step 1 — Creating SSH Keys

```
ssh-keygen 

```
- file in which to save the key (/home/username/.ssh/id_rsa):

- The private key will be called id_rsa and the associated public key will be called id_rsa.pub.

- Step 2 — Copying an SSH Public Key to Your Server
   - cat ~/.ssh/id_rsa.pub 
   - ~/.ssh/authorized_keys/id_rsa.pub

- Step 3 — Authenticating to Your Server Using SSH Keys

```
ssh username@remote_host
```
- Step 4 — Disabling Password Authentication on your Server

```
sudo nano /etc/ssh/sshd_config
```
```
PasswordAuthentication no
```
```
sudo systemctl restart ssh
```

- You should now have SSH key-based authentication configured and running on your server, allowing you to sign in without providing an account password