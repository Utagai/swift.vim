# Notice

This is a fork of Keith Smiley's project, and its only difference (at
this point) is the use of a different indent file as his was causing lots of
issues with the Swift codebase I am working on (and no, it's not a horribly
formatted one, so it shouldn't be a pathological example). The ['new' indent
file](https://github.com/kballard/vim-swift) that replaces Keith's is taken from
Kevin Ballard.

In other words, I deserve no credit for owning this fork. Almost all the credit
goes to Keith Smiley's great work, as well as Kevin Ballard for his indent file.

There is also a small change I have made by adding a match rule for column
widths. This is useful for highlighting lines that exceed a column width. I use
this personally, and it is cleaner for me if the rule is set externally and all
I have to do is set the Highlight on the match rule name, but in either case,
this is an exceedingly minor change and I still deserve no credit.

It is possible that I will make smaller changes in the future, but for the most
part, I will just follow Keith's changes and fixes on his/the main project.

# Swift.vim

Syntax and indent files for [Swift](https://developer.apple.com/swift/)

If you don't have a preferred installation method check out
[vim-plug](https://github.com/junegunn/vim-plug).

## Examples

![](https://raw.githubusercontent.com/keith/swift.vim/master/screenshots/screen.png)
![](https://raw.githubusercontent.com/keith/swift.vim/master/screenshots/screen2.png)

## [Syntastic](https://github.com/scrooloose/syntastic/) Integration

swift.vim can show errors inline from
[swift package manager](https://github.com/apple/swift-package-manager/)
or from [swiftlint](https://github.com/realm/SwiftLint) using
[syntastic](https://github.com/scrooloose/syntastic/).

![](https://raw.githubusercontent.com/keith/swift.vim/master/screenshots/screen3.png)

### Usage

- Install [syntastic](https://github.com/scrooloose/syntastic/)

- swiftpm integration will be automatically enabled if you're running vim
from a directory containing a `Package.swift` file.

- SwiftLint integration will be automatically enabled if you have
SwiftLint installed and if you're running vim from a directory
containing a `.swiftlint.yml` file.

- To enable both at once add this to your vimrc:

```vim
let g:syntastic_swift_checkers = ['swiftpm', 'swiftlint']
```
