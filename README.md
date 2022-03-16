## Make the keyfolder:

```
cd
mkdir TEMPKEYS
cd TEMPKEYS
ssh-keygen -t ed25519 -C "emailaddress@for.github"
# This will prompt where to save it - you want to enter
/Users/yourname/TEMPKEYS/id_ed25519
# It will prompt for a passphrase for the keys - up to you whether to use
```

## Tell your ssh-agent to look in that folder for keys whaen doing ssh-things:

```
ssh-add -K ~/TEMPKEYS/id_ed25519
# Note: if you didn't use a passphrase, you don't need the -K flag
# Some MacOS versions don't support the -K, so get rid of it if needed
```

## Copy your *public* key to github

go to githup -> sign in -> profile icon -> Settings -> SSH and GPG keys -> Add new SSH key

## Done!
