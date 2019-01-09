# git-commit-auto-message

Commit with a generic commit message based on the first staged filename and
action performed on the file.

For cases, when you possibly couldn't come up with a better commit message or it
simply doesn't matter.

```sh
$ git status -s
A  image.png

$ git-commit-auto-message
[master a61951a] add image.png
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 my-image.png

$ git mv image.png hello.png
$ git-commit-auto-message
[master b48759f] rename image.png to hello.png
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename image.png => hello.png (100%)

$ git log
b48759f rename image.png to hello.png
a61951a add image.png
```
