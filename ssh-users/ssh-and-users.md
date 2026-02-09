# SSH & User Management Documentation

## Non-Root User Creation

I created a new user to avoid working directly as root.

Commands used:

sudo adduser devops  
sudo usermod -aG sudo devops  

This grants administrative privileges safely.

---

## Switching Users

I switched to the new user using:

su - devops

---

## SSH Key Authentication

I generated SSH keys locally:

ssh-keygen

Then copied the public key to the server:

ssh-copy-id devops@server_ip

This enabled passwordless login.

---

## Why Root Login is Unsafe

Root login is discouraged because:

- Full system control increases risk
- Vulnerable to brute-force attacks
- No activity traceability
- Violates least-privilege principle

Using a sudo user improves security.

---

## Permissions Management

I practiced file permissions using:

chmod  
chown  

Example:

mkdir project-files  
sudo chown devops:devops project-files  
chmod 755 project-files  

ls -l output was used to verify permissions.

---

## Proof of Access

(Screenshot of SSH login without password will be attached)
