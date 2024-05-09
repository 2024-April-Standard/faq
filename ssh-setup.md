# SSH Key Setup


## For WINDOWS USERS ONLY

- Run as Administrator "Windows PowerShell
- Download Ubuntu via Windows Powershell -> Type "wsl --install
- Wait for that to downloa
- Restart Your PC

## All Users
- Create a GitHub Account With a Unique Email and Username on GitHub.com

> **Remember this email and username**
  
- ** Windows ONLY** Open up Ubuntu (go to menu on your PC and type in Ubuntu)
- Type `git config --global user.name <insertYourGitHubUsernamehere>` (dont add <>)
- Type `git config --global user.email <insertYourGitHubEmail>`
- Type `cat .gitconfig` 
> **NOTE** Check to see if your username and email match GitHub Account

- Type `ssh-keygen -C <yourEmailUsedInGitHubSignUpHere>` (dont add <>)
- When it prompts enter file hit "Enter" key to use default destination pathway
- Enter a passphrase (this wont be visible while you type)
- Press `Enter` Key
Enter Password Again

Type `eval "$(ssh-agent -s)"`

type in -> `ssh-add ~/.ssh/id_rsa` 
> **NOTE** You might have a different name for your ssh key, for example id_ed25519 use that instead of id_rsa If you're unsure, use `ls ~/.ssh`

Password Prompt will popup, Re-enter your password

Hit `Enter` Key

Type `cat ~/.ssh/id_rsa.pub`
> **NOTE** Shows your public key which youll need for GitHub

- Copy the whole Key generate
- Open up GitHub.Com and Login
- Go to top right corner where your profile icon is
- Go to Settings
- Go to SSH and GPG Keys
- Click New SSH Key
- Paste the Code into the box

Done! (Hopefully)

To test this config has worked run `ssh -T git@github.com`
If successful, after accepting GitHub’s keys, it should return a message with your GitHub username saying you’ve successfully authenticated.
If it gives you an error, feel free to post a screenshot or paste of your terminal. Make sure to include all text even if you don’t think it’s relevant!
