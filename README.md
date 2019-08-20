# Setting up SSH keys (Git bash or terminal)

- Copy and paste to your terminal to generate new ssh key

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- On the next screen where it says "Enter a file in which to save the key," press enter to save in default location.

```
> Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]
```

- On the next prompt enter a password you will easily remember.

```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

- Copy and paste to your terminal to make sure ssh agent is running.

```
eval $(ssh-agent -s)
```

- You should get a prompt that looks like this. Your pid number will be differnet.

```
> Agent pid 59566
```

- Copy and paste to your terminal to add the ssh key to your ssh agent.

```
ssh-add ~/.ssh/id_rsa
```

- Copy and paste to your terminal to copy the ssh key to your clipboard.

```
$ clip < ~/.ssh/id_rsa.pub
```

# On Github

- Click your icon on the right hand of the screen.
- Select settings in menu.
- Select SSH & GPG keys.
- Select New SSH key.
- Paste ssh key - You copied the ssh key to your clipboard with the clip comand earlier.
