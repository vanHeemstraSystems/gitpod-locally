# 100 - Getting Started

1. Download the [latest release](https://github.com/gitpod-io/run-gp/releases/latest).
> If you're on MacOS you'll need to jump through hoops because the run-gp releases are not signed.

2. In a terminal navigate to a directory containing a ```.gitpod.yml``` file, e.g. a Git working copy of a repository, then execute ```run-gp```.

```
$ git clone https://github.com/gitpod-io/go-gin-app
$ cd go-gin-app
$ run-gp
```

**Note**: The ```run-gp``` command will use the current working directory as context. To point it to a different directory, use the ```-w``` option.

3. Once the workspace is ready, open the URL displayed in the terminal.
