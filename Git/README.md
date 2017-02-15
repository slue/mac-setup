# Git and GitHub

What's a developer without [Git](http://git-scm.com/)? To install, simply run:

```
$ brew install git
```

When done, to test that it installed fine you can run:

```
$ git --version
```

And `$ which git` should output `/usr/local/bin/git`.

Next, we'll define your Git user \(should be the same name and email you use for [GitHub](https://github.com/)\):

```
$ git config --global user.name "Your Name Here"
$ git config --global user.email "your_email@youremail.com"
```

They will get added to your `.gitconfig` file.

### DS\_Store

On a Mac, it is important to remember to add `.DS_Store` \(a hidden OS X system file that's put in folders\) to your `.gitignore` files.

* * -

### Setting up Sublime Text as the Git Mergetool

```
$ git config --global mergetool.sublime.cmd "subl -w \$MERGED"
$ git config --global mergetool.sublime.trustExitCode false 
$ git config --global merge.tool sublime
$ git mergetool -y
```



