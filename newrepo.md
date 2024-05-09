# Creating a GitHub Repository 

  1. Login GitHub.com
2. Top Right Hand Corner (Icon) Click "Your Repositories"
3. Click Green Icon "New"
4. Name your folder whatever you like
5. Open up your terminal (Ubuntu on WSL for Windows Users)
6. `mkdir <folderName>`
    1.  Makes a Parent Directory named`folderName`
7. `cd <folderName>` 
    1. Change Directory into `folderName`
8. `git init`
    1. Creates a new local repository for `folderName`
9. Create a file, can be anything. By convention this is usually a `README.md` file, however can be anything.
10. `git add .`
    1. Adds any changes made in the working folder to the staging area
    2. To stage changes only in a single file, you can type the file name instead of `.`
    3. For example, `git add README.md`
11. `git commit -m “<message>”`
    * Commits your staging area into the history.
12. `git branch -M main`
    1. This command forces you to be committing to the `main` branch. If the `main` branch doesn’t exist, it will create it. 
13. `git remote add <name> <remote>`
    1. This command links a repository that’s not hosted on your machine to the repository that’s on your machine.
    2. There is a `<name>` variable as you can name the remote repository anything, however, by convention it is usually called `origin`
    3. `<remote>` refers to the HTTPS **OR** SSH URL of your remote repository.
    4. **IMPORTANT FOR THIS COURSE** As we’ve set up SSH keypairs, make sure to use an SSH link for your remote, this will look like `git@github.com:<yourGitHubUsername>` if your remote starts with `https://` you’re using HTTPS which will prompt you to enter your credentials every time you push.
14. `git push origin main`
    1. Assuming you named your remote and branches according to convention, this command will push your commit history  to the main branch on the remote repository.
15. `code .`
    1. Launches VS Code in your working directory
