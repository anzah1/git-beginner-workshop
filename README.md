# First steps

- Install [Git](https://git-scm.com)

- Unless you know really what you want, choose defaults on install

- Launch Git Bash (for simplicitly rest of the instructions assume that Git
  Bash is used)

- Configure your name to Git

```bash
git config --global user.name "I Don't Know How To Change Parameters"
```

- Configure your e-mail address:

```bash
git config --global user.email i_like@defaults.com
```

- Configure default editor (vim and notepad are available by default on Windows
  without setting full path to the executable):

```bash
git config --global core.editor notepad
```

- Remember if you're wondering what any command does, you can open help for
  that command:

```bash
git help config
```

- For more information, there's [Pro Git book](https://git-scm.com/book/en/v2)

# Beginner assigment

- Clone repository from [git-beginner-workshop](https://github.com/anzah1/git-beginner-workshop.git)

- If you're doing this alone and not in a workshop, you can clone this GitHub
  repository and then clone that as your working copy:

```bash
git clone --bare 'https://github.com/anzah1/git-beginner-workshop.git'
git clone git-beginner-workshop.git git-beginner-workshop
```

## Create a file

- First task is to create a file that is named after you

- You can edit files in working copy of the repository with any tool you like
  (Git Bash is not required)

- Just for sake of example here's how to do it from Git Bash:

```bash
cd git-beginner-workshop
touch your_name
```

- If you actually use `your_name` literally, in workshop situation you
  voluntarily enrolled for Git merge conflits course

## Check the repository status

- Check the repository status:

```bash
git status
```

- File you created shows up under untracked files

- That means that Git knows about the file, but it's not part of the repository
  history yet

- Remember that `git status` is trying to be helpful, read what it says

## Prepare things for making a commit

- To show your intention of tracking version of any file (or directory) use git
  add:

```bash
git add your_name
```

- If you run `git status` again, file is no longer in list of untracked files

- If ran `git status` file is now in list of files to be commited

- `git add` can be run multiple times in order to add more files into a commit

## Make commit

- Let's do a commit now:

```bash
git commit
```

- Editor you configured should open

- Describe what you did and why you did it

- First line is very consice summary of the change

- From third line onwards, you can have more detailed explanation

- Remember to keep the second line always empty

- One you're done, save the file and quit the editor

## Synchronize repository and publish your changes

- It's good idea to synchronize the repository before trying to push the changes

- Pull changes from the remote repository:

```bash
git pull
``` 

- Gits pull operation gets the latest changes

- Push your changes

```bash
git push
```

- If there's error message, most likely you need to pull again in order to push
