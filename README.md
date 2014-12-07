# Git Commit Photo
** Post-commit git hook to capture a snapshot from the isight camera after a git commit **


## How

Install imagesnap ( utility to take a snapshot from the command line )
``` 
brew install imagesnap
```

Make a directory to store the global hooks and set it on the global config
```
mkdir -p ~/.git-templates/hooks
git config --global init.templatedir '~/.git-templates'
```
This will copy everything in the git-templates folder to the project every time a repo is cloned or initialized

Then add the post-commit hook to '~/.git-templates/hook/post-commit'
```
cp ./post-commit ~/.git-templates/hook/post-commit
```

Make it executable
```
chmod a+x ~/.git-templates/hooks/post-commit
```

To make this work in existing repos just run
```
git init
```

