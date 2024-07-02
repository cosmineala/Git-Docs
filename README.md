# Git-Docs

## Config git with SSH

- Install Git

- Enable SSH Agent
```powershell
# Have ssh agent start automatically
Get-Service ssh-agent | Set-Service -StartupType Automatic

# Start ssh agent now
Start-Service ssh-agent

# Should work successfully
Get-Service ssh-agent
```

- Configure GIT with SSH agent
```powershell
# tell git to use ssh.exe
git config --global core.sshCommand "'C:\Windows\System32\OpenSSH\ssh.exe'"
```

- Generate key pair
```powershell
ssh-keygen -o -t rsa -C "<EMAIL_ADDRESS>"
```

- Register key
```powershell
ssh-add "C:\Users\<USERNAME>\.ssh\<KEY_FILE>" 
```

- Register key to Online GIT provide

- Clone repo
```powershell
git clone "<git@github.com:cosmineala/Git-Docs.git>"
```

- Configure global GIT user
```powershell
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```


