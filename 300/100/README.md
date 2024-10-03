# 100 - Getting Started

1. Download the [latest release](https://github.com/gitpod-io/run-gp/releases/latest). **Note**: Our Mac Mini with Intel Core i5 processor uses an ```amd64``` architecture.
> If you're on MacOS you'll need to jump through hoops because the run-gp releases are not signed.
>
> MacOS requires that binaries downloaded using a browser must be [signed and notarized](https://developer.apple.com/developer-id/).
> 
> Otherwise you won't be able to just execute the `run-gp` command. If you download the release using `curl` in a terminal, MacOS will just let you execute the binary. ```$ curl -L https://github.com/gitpod-io/run-gp/releases/download/v0.1.7/run-gp_0.1.7_Darwin_amd64 > run-gp```
>
> Move the executable to the Applications directory: ```$ mv run-gp /Applications/run-gp```
>
> Go to the Applications directory: ```$ cd /Applications```
> 
> Run the following command to set the file's executable bit using the chmod command: ```$ chmod +x ./run-gp```
>
> It requires Docker deamon, so make sure you have Docker deamon running.
>
> If Docker is not installed:
> 1) Install [Docker Desktop for Mac](https://docs.docker.com/docker-for-mac/install/) or use ```$ brew install homebrew/cask/docker```.
> 2) Run it and pass admin credentials to start everything
>
> Then you can run it with ```$ /Applications/run-gp```. Try ```$ /Applications/run-gp --help``` for details instructions.
>
> To [Add the run-gp executable to the PATH variable](https://pimylifeup.com/macos-path-environment-variable/), create a new file within the “/etc/paths.d” directory: ```$ sudo nano /etc/paths.d/run-gp```
>
> Now, inside the newly created file ```run-gp``` you simply need to add the path that you want added to your macOS path environment variable: ```/Applications/run-gp```
>
> After making these changes, save and quit by pressing CTRL + X, followed by Y, then the ENTER key.
>
> Now close out of the current terminal session and open a new one.
>
> The changes won’t affect anything currently running as they need to re-read the path environment variable.
>
> With a new terminal session open, let us check the contents of the macOS path environment variable by using the command: ```$ echo $PATH```
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
