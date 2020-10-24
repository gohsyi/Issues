Homebrew updateing is extremely Slow

```
$ #cd to homebrew foler
$ cd "$(brew --repo)"；
$ #check  git remote status
$ git remote -v;
https://github.com/Homebrew/homebrew.git
$ #update remote url with Coding.net
$ git remote set-url origin https://git.coding.net/homebrew/homebrew.git
$ brew update
```
