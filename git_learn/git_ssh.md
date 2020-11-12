# SSH link to GIT

## Question: how to link local git repository to remote github?

**- generate a new ssh key**

1. open git bash
2.  > $ ssh-keygen -t ed25519 -C "your_email@example.com"
   
    This creates a new ssh key, using the provided email as a label.
    > Generating public/private ed25519 key pair.
3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
    > Enter a file in which to save the key (/c/Users/you/.ssh/id_ed25519):[Press enter]
4. At the prompt, type a secure passphrase. 
    > Enter passphrase (empty for no passphrase): [Type a passphrase]
    
    > Enter same passphrase again: [Type passphrase again]