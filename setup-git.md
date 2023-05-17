# Setup git on WSL

## Installation
For Ubuntu, this PPA provides the latest stable upstream Git version
```
sudo add-apt-repository ppa:git-core/ppa
```
```
sudo apt update
```
```
sudo apt install git
```

## Check for SSH key already generated
1. Check if you already have an SSH key by running the following command:
```
ls ~/.ssh
```
2. If no files in the '~/ssh' directory, you need to generate SSH

## Generate SSH
1. Generate a new SSH key pair by running the following command:
```
ssh-keygen -t rsa -b 4096 -C "your@email.com"
```
Email must be associated with github account
2. Choose default location ('~/ssh/id_rsa') and no passphrase
3. Display the public key by running
```
cat ~/.ssh/id_rsa.pub
```

4. Go to your GitHub account in your web browser and log in.

5. Click on your profile picture in the top right corner and select "Settings" from the dropdown menu.

6. In the left sidebar, click on "SSH and GPG keys."

7. Click on the "New SSH key" button.

8. Give your SSH key a suitable title, such as "WSL SSH Key."

9. Paste the copied public key into the "Key" field.

10. Click on the "Add SSH key" button to save it.

## Config git
1. Configure your Git username and email by running the following commands:
```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```
2. Use SSH protocols for repositories
