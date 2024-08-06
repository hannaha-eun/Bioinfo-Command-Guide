##  Git SSH key
Guide for setting up a ssh key to use for authentication for github 

### 1. Key generation
   
   1.1 Below command creates a new SSH key, using the provided email as a label.   

` ssh-keygen -t ed25519 -C "my_email@example.com" `
   
   1.2 Press Enter to accept the default file location when "Enter a file in which to save the key" is printed.   
      
   
   1.3  type a secure passphrase.    


### 2. Adding a new SSH key to the ssh-agent   
   
   2.1 Start the ssh-agent in the background.
   `eval "$(ssh-agent -s)" `
      
   2.2 Add  SSH private key to the ssh-agent.   
   (replace the name of the key file when needed)
   `ssh-add ~/.ssh/id_ed25519 `


### 3. Adding a new SSH key to GitHub account
   
   3.1 Copy the SSH public key    
   `cat ~/.ssh/id_ed25519.pub  `
   
   3.2 Go to Settings > Access > SSH and GPG keys on GitHub  
      
   3.3 "Click New SSH key" or "ADD SSH key"   
      
   3.4 Enter Title, type of key, copy ssh key to "Key" field
      
   3.5 Add SSH Key
