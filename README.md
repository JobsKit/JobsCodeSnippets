# Jobs.iOS.Codesnippets

整理这个代码片段集的初衷有以下几点：

* 我们发现由于 Xcode 本身的功能不足，导致我们经常在重写一些系统父类方法时容易忘了调用 `super`，从而出现一些很难排查的诡异bug。

* Xcode 虽然有模糊匹配的代码提醒，但代码提醒只能帮你写方法名，而code snippets 还可以帮你填充一些默认的方法实现，或者直接移动光标到方法体内，省去几次光标操作。

* 一些常用的写法本身语法可能比较复杂，难以记忆，例如实现一个类的单例、使用 `swizzle` 来重写系统控件的方法、block 在不同地方的语法不同等。

* 一些代码本身看似简单，但由于特别常用，所以使用 code snippets 可以大大节省时间。

## 使用方式

Xcode 的 Code Snippets 文件存放于 `~/Library/Developer/Xcode/UserData/CodeSnippets` 目录，只要直接把 `*.codesnippets` 文件放到这个目录下（若没有则自己创建），重启 Xcode 即可生效。

为了方便更新，建议直接将 QMUI iOS CodeSnippets clone 到这个目录内（注意，不是在 CodeSnippets 里创建一个 QMUI 的目录，这里不支持子目录）：
```bash
cd ~/Library/Developer/Xcode/UserData/CodeSnippets
```
CodeSnippets 目录为空:
```bash
git clone https://github.com/QMUI/QMUI_iOS_CodeSnippets.git ./
```
CodeSnippets 目录不为空:
```bash
git init .
git remote add origin https://github.com/QMUI/QMUI_iOS_CodeSnippets.git
git pull origin master 
```
