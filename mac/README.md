### Homebrew updateing is extremely Slow

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

### Set 自然码 as the default input method
```
$ defaults write com.apple.inputmethod.CoreChineseEngineFramework shuangpinLayout 5
```
