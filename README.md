# git cheat sheet

## Git readme styling
https://guides.github.com/features/mastering-markdown/

All commands in this page will use https://github.com/arvidjohansen/git-cheat-sheet as the example of a repo

## Clone a repo to a new folder
1. Create a new repo 
1. Clone it to a folder with the following command:
```Sh
git clone https://github.com/arvidjohansen/git-cheat-sheet
```
This is usually the best way to do things, since you can start working on a working repo right away. However, if you already started writing code, you will want to use the following method:

## Add existing code to a new repo
1. Create a new repo and copy the link (don't create a readme.md), in my case: https://github.com/arvidjohansen/git-cheat-sheet

Navigate to the folder containing your code and run the following commands:
```sh
echo "# git-cheat-sheet" >> README.md # creates a readme file
git init # initializes the repository
git add README.md # adds the readme file to the repo
git commit -m "first commit" # creates a new commit with  the message "first commit"
```

Now we have initializes a new reposity, added a file and committed it. 
Before we can upload it, we need to rename our current branch to "main" with the following command:

```sh
git branch -M main
```
Now we are ready to upload our file, but first we need to tell git where to upload it:
```sh
git remote add origin https://github.com/arvidjohansen/git-cheat-sheet.git
```

That's it, we are ready to push our changes.

The first time we run the push-command, we need to tell git that we want this to be our default target from now on with the -u parameter:
```sh
git push -u origin main
```
Enter your username and password and we are done.

## Working with an initialized repo
No matter which method you used to create your repo, you are now ready to start coding and let git track the changes.

To view the status of tracked and untracked files use:
```sh
git status
```

Each time you want to push a change there is 3 steps you have to do:
1. Add the files you want to push:
```sh
git add <filename>
```
2. Commit the changes with a proper commit message:
```sh
git commit -m "Fixed bug in the whatever module"
```
3. Push the changes:
```sh
git push
```

That's it.

If someone else committed changes while you were on vacation, use the pull-command to download the changes:
```sh
git pull
```

If you are lucky, there won't be merge conflicts.

Good luck!

## How to make cool formating in README.md, comments etc
Read [getting started with writing and formatting on github](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github) by @github

Also [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) by @github

or [download the pdf](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

And here is what the pdf's look like:


![page-1](https://i.postimg.cc/NMwRtcpL/git-cheat-sheet-1.png)

![page-2](https://i.postimg.cc/L6sL2vBk/git-cheat-sheet-2.png)


also https://github.github.com/gfm/


## Renaming a repository
1) Make sure you are up to date with your remote
```sh
git push && git pull
```

2) Rename your repository under settings -> repository name

3) Update your repo with following command:
```sh
git remote set-url origin <your-new-url>
```

## Creating template-repositories
[Guide on creating template-repositories](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template)

## Emojis
* [Emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)




