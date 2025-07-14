# github SSH authentication
## generate an ssh key pair
`ssh-keygen -t ed25519 -c "YOUR_EMAIL@gmail.com"`
## add your ssh key to ssh agent
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
## copy your public key [copy all output]
`cat ~/.ssh/id_ed25519.pub`
## [add your ssh key to github](https://github.com/settings/keys)
- New SSH Key
## test your ssh connection
`ssh -T git@github.com`
