
### Syntax
`ansible-playbook -i hosts.ini reset_password.yml --extra-vars "new_password=NEW_PASSWORD_HERE"`

### Example
`ansible-playbook -i hosts.ini reset_password.yml --extra-vars "new_password=myNewSecurePassword123"`

### Additional Info
For IOS/IOS-XE, secret 0 is used, meaning the password is stored in plain text. You can modify this to use encrypted formats (secret 5 for MD5 or secret 9 for SHA-256).

For IOS-XR, you can define different encryption methods depending on your needs.

- Encryption: If you need to store passwords as encrypted secrets, modify the secret 0 to secret 5 or secret 9 depending on the type of encryption you need for IOS/IOS-XE devices.
