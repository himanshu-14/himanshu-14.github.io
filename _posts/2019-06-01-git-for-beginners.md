# GIT VERSION CONTROL FOR ABSOLUTE BEGINNERS

## Let's get started
People say git is an open source distributed version control system blah blah..
But simply put git is a small applivation you install on your computer that can keep track of any changes in a folder of files.
Download this small app from here depending upon your OS( Windows/Linux/Mac Os)
https://git-scm.com/downloads
Install it with all defaults and tada you're ready for gitting gud.

so all you need to do is open up your Command prompt ( I am assuming that most git beginners like I once was are on Windows because if you're on linux you probably know git) 
You can do this by typing cmd on run or just search for cmd in thr start menu.
Your command propmt shows the current folder you are in.
So go ahead and create a new folder in your C drive name it something short like git-repos and cd into it
cd C:/git-repos/
create a new folder inside this folder either through Windows Explorer or just by typing
mkdir my-first-git-repo
cd my-first-git-repo to change your current directory(fancy name for a folder) to the folder you just created.
Now you create new files inside this folder.
Create 2 files say 1 text file notes.txt amd another word file mydoc.docx
Once you have created the files put some text into those files.
Just a few lines maybe and save them
Now you have these 2 files and you need a way to keep track of the changes you make in each file. 
so all you do is in your command prompt (ensuring current folder is my-first-git-repo)
Run git init
When you installed git it performed some magic or rather added it's folder to your PATH environment variable.
That is where Windows looks for executable files when you run a vommand.
So when you say git Windows runs git by finding it from your PATH environment variable.
and init is a command that tells git to initialise a new repository.
Just a way of saying hey git keep track of the files in this folder for me please.
git like an obedient child creates a .git hidden folder inside your folder where it magically stores all the info it needs to keep track of your files.
So now you have a folder with 2 files converted to a git repository.
Now you make changes in the 2 files. Because well you love making notes and so you update your files with some more text.
You save the 2 files notes.txt and mydoc.txt
and then again in your cmd in the directory my-first-git-repo you run
git status
Congrats git tells you you've made changes to notes.txt and mydoc.doc
git also gives you some measages about staging these changes and committing them which is how the creator of git wanted to scare beginners away.
Git has in a way taken a snapshot of your files in when you rand the init command.
Now it knows the snapshot it took earlier looks different from the current snapshot.
So it wants to create another snapshot but it won't do that till you tell it to.
You also need to tell it what to keep in the next snapshot.
A snapshot is called a commit in git jargon.
So now you run git add . command 
To tell git that in the next commit keep the changes to all files in this folder.
That is stage all the changes.
You could also have said git add notes.txt to just add notes.txt to the next snapshot and there are sometimes reasons to do that as well but for now we will be adding all files
You can check what git add . did by running git status again.
And viola! git has staged both the files or rather the changed in both files to be put in the next commit.


Then finally you run git commit -m "modified notes.txt and mydoc.docx"
This command tells git to take the snapshot again with the changes.
Also each commit has an associated message so someone can see your commit history and make sense of what you did over time.

You can run git satus again to see that hit is happy that the latest snapshot it has and the files in your folder are the same.
Make git unhappy again by making changes in your notes.txt and saving it.
Run git status and git is sad its latest snapshot doesnt look like your folder and tells you you modfied notes.txt
run git add .
followed by git commit -m "updated notes.txt"
Folllwed by git status 
You'll see git is happy as you have committed your changes.

Time to up your game a bit and add remotes to this scenario.
Git has what are called remotes or remote repositories.
so your local gir rep here called my-first-git-repo this repo doesn't have any remotes right now
Each remote has a name and by convention the main remote is called origin.

You go to github create a free account and then create a new repository in the web based gui it provides.
git might ask you if you want to create a readme.md but dont check that.
Just create a blank repo.
Once you have the blank repo open the main repo page and you will see a clone url

so you run
git remote add origin 







