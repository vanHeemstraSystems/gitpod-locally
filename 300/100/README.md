# 100 - Getting Started

1. Download the [latest release](https://github.com/gitpod-io/run-gp/releases/latest). **Note**: Our Mac Mini with Intel Core i5 processor uses an ```amd64``` architecture.
> If you're on MacOS you'll need to jump through hoops because the run-gp releases are not signed.
>
> MacOS requires that binaries downloaded using a browser must be [signed and notarized](https://developer.apple.com/developer-id/).
> 
> Otherwise you won't be able to just execute the `run-gp` command. If you download the release using `curl` in a terminal, MacOS will just let you execute the binary. ```$ curl -L https://github.com/gitpod-io/run-gp/releases/download/v0.1.7/run-gp_0.1.7_Darwin_amd64 > run-gp```
>
> Alternatively, you can head over to the `Security` system settings and allow the binary to run once MacOS denied this on the first attempt.

2. In a terminal navigate to a directory containing a ```.gitpod.yml``` file, e.g. a Git working copy of a repository, then execute ```run-gp```.

```
$ git clone https://github.com/gitpod-io/go-gin-app
$ cd go-gin-app
$ run-gp
```

**Note**: The ```run-gp``` command will use the current working directory as context. To point it to a different directory, use the ```-w``` option.

3. Once the workspace is ready, open the URL displayed in the terminal.
