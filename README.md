# Setting up SSH keys (Git bash or terminal)

- Copy and paste to terminal

_Generates a new ssh key attached to your email address. Make sure to fill in YOUR email._

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- On the next screen where it says "Enter a file in which to save the key," press enter to save in default location.

```
> Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]
```

- On the next prompt enter a password you will easily remember

```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

- Copy and paste to terminal

_Makes sure the ssh agent is running_

```
eval $(ssh-agent -s)
```

- You should get a prompt that looks like this (your pid number will be differnet)

```
> Agent pid 59566
```

- Copy and paste to terminal

_Adds ssh key to ssh agent_

```
ssh-add ~/.ssh/id_rsa
```

- Copy and paste to terminal

_Copies the ssh key to your clipboard_

```
$ clip < ~/.ssh/id_rsa.pub
```

# On Github

- Click your icon on the right hand of the screen
- Select settings in menu
- Select SSH & GPG keys
- Select New SSH key
- Paste ssh key
