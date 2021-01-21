---
title: SSH installation
tags: []
---

## How to Setup SSH keys
Secure Shell (SSH) is a network protocol for creating a secure connection between a client and a server. With SSH, you can run commands on remote machines, create tunnels, forward ports, and more.

### Creating SSH key on Windows
#### Step 1. Run the below command on cmd console:
> ssh-keygen -t rsa -b 4096 -C "your_email@domain.com"

You will be prompted to specify the file name:
> Enter file in which to save the key (/home/yourusername/.ssh/id_rsa):

The default location and file name should be fine for most users. Press Enter to accept and continue.

Next, you’ll be asked to type a secure passphrase. A passphrase adds an extra layer of security. If you set a passphrase, you’ll be prompted to enter it each time you use the key to login to the remote machine.

If you don’t want to set a passphrase, press Enter.

#### Step 2. Verify that the new key was created 
Go to the below path:
> C:\Users\<user>\.ssh

That’s it. You’ve successfully generated an SSH key pair on your Ubuntu client machine

#### Step 3. Copy the SSH key to the server
Run the below command on the console:
> ssh-copy-id remote_username@server_ip_address


#### Step 4. Login to the server using the ssh key
Run the below command on the console
> ssh remote_username@server_ip_address
