
# To check current credentials

        git config --global user.name
        git config --global user.email

## To set global level credentials

        git config --global user.name
        git config --global user.email

## To set repo level credentials

        git config user.name
        git config user.email

## working with 2 different account. the above first solution worked for me, as i was having mac system

Setting Global Git Username and Email
The global git username and email address are associated with commits on all repositories on your system that don’t have repository-specific values.

To set your global commit name and email address run the git config command with the --global option:

git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"
CopyCopy
Once done, you can confirm that the information is set by running:

git config --list
Copy
user.name=Your Name
user.email=youremail@yourdomain.com
Copy
The command saves the values in the global configuration file, ~/.gitconfig:

~/.gitconfig
[user]
    name = Your Name
    email = youremail@yourdomain.com
Copy
You can also edit the file with your text editor, but it is recommended to use the git config command.

Setting Git Username and Email for a Single Repository
If you want to use a different username or email address for a specific repository, run the git config command without the --global option from within the repository directory.

Let’s say you want to set a repository-specific username and email address for a stored in the ~/Code/myapp directory. First, switch the repository root directory:

cd ~/Code/myapp
Copy
Set a Git username and email address:

git config user.name "Your Name"
git config user.email "youremail@yourdomain.com"
CopyCopy
Verify that the changes were made correctly:

git config --list
Copy
user.name=Your Name
user.email=youremail@yourdomain.com
Copy
The repository-specific setting are kept in the .git/config file under the root directory of the repository.
