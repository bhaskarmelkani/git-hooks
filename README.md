# git-hooks
Git hooks to deploy code to server.


Create a project directory.
> mkdir project;

Go to that directory.
> cd project;

Clone your git repository here.
> git clone https://github.com/example/myCode.git;

Create a git directory for bare repository.
> mkdir myCode.git;

Go the the bare git directory.
> cd myCode.git;

Create a git bare repository.
> git init --bare;

Create a post recieve hook and save it.
> vim hooks/post-receive

Give it executable permissions. Use the content of hooks/post-revieve from the files 
> chmod ug+x hooks/post-receive


- Now any one having access to this server can push code to it by creating a remote in their local repo.
Adding git remote for pushing code to server. 
git remote add myServer user@<server's ip>:<path to this folder>/project/myCode.git.
git remote add myServer root@10.10.1.1:/var/www/project/myCode.git.

Pushing code to server.
git push myServer master;

