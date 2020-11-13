# SSH link to GIT

## Question: how to link local git repository to remote github?

**- generate a new ssh key**

1. open git bash
2.  > $ ssh-keygen -t ed25519 -C "your_email@example.com"\
    (i used qbu@connect.ust.hk)
   
    This creates a new ssh key, using the provided email as a label.
    > Generating public/private ed25519 key pair.
3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
    > Enter a file in which to save the key (/c/Users/you/.ssh/id_ed25519):[Press enter]
4. At the prompt, type a secure passphrase. 
    > Enter passphrase (empty for no passphrase): [Type a passphrase]
    
    > Enter same passphrase again: [Type passphrase again]

**- add ssh key to ssh-agent**

1. start ssh-agent manually
    > \# start the ssh-agent in the background \
    $ eval $(ssh-agent -s)\
    \> Agent pid 59566
2. Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.
    > $ ssh-add ~/.ssh/id_rsa\
    (my own key file: /c/Users/BU/.ssh/id_ed25519.pub)
3. add the ssh key to github account

**- add a new ssh key to github account**

1. copy the ssh key to clip board\
If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.
    > $ clip < ~/.ssh/id_rsa.pub\
    \# Copies the contents of the id_rsa.pub file to your clipboard
2. In the upper-right corner of any page, click your profile photo, then click Settings.
3. 