# 100 - Getting Started

1. Download the [latest release](https://github.com/gitpod-io/run-gp/releases/latest). **Note**: Our Mac Mini with Intel Core i5 processor uses an ```amd64``` architecture.
> If you're on MacOS you'll need to jump through hoops because the run-gp releases are not signed.
>
> MacOS requires that binaries downloaded using a browser must be [signed and notarized](https://developer.apple.com/developer-id/).
> 
> Otherwise you won't be able to just execute the `run-gp` command. If you download the release using `curl` in a terminal, MacOS will just let you execute the binary. ```$ curl -L https://github.com/gitpod-io/run-gp/releases/download/v0.1.7/run-gp_0.1.7_Darwin_amd64 > run-gp```
>
> Move the executable to the ```usr/local/bin``` directory: ```$ mv run-gp /usr/local/bin/run-gp```
>
> Go to the directory: ```$ cd /usr/local/bin```
> 
> Run the following command to set the file's executable bit using the chmod command: ```$ chmod +x ./run-gp```
>
> It requires Docker deamon, so make sure you have Docker deamon running.
>
> If Docker is not installed:
> 1) Install [Docker Desktop for Mac](https://docs.docker.com/docker-for-mac/install/) or use ```$ brew install homebrew/cask/docker```.
> 2) Run it and pass admin credentials to start everything
>
> Then you can run it with ```$ /usr/local/bin/run-gp```. Try ```$ /usr/local/bin/run-gp --help``` for details instructions.
>
> There is no need to [Add the run-gp executable to the PATH variable](https://pimylifeup.com/macos-path-environment-variable/) as the /usr/local/bin directory is already pat of the PATH variable.
>
> So, you can run ```run-gp``` from any directory on your Mac.
>
> Alternatively, you can head over to the `Security` system settings and allow the binary to run once MacOS denied this on the first attempt.

2. In a terminal navigate to a directory containing a ```.gitpod.yml``` file, e.g. a Git working copy of a repository, then execute ```run-gp```.

```
$ git clone https://github.com/gitpod-io/go-gin-app
$ cd go-gin-app
$ run-gp
```

**Note**: The ```run-gp``` command will use the current working directory as context. To point it to a different directory, use the ```-w``` option.

**Warning**: You may see this error:
docker: Error response from daemon: Mounts denied: 
 The path /users/willemvanheemstra/git/go-gin-app is not shared from the host and is not known to Docker.
 You can configure shared paths from Docker -> Preferences... -> Resources -> File Sharing.
 See https://docs.docker.com/desktop/mac for more info.

Follow the advice given. In Docker Deskop on MacOS configure shared paths from Docker Desktop: Settings > Resources > File Sharing. Add an extra entry ```/users/willemvanheemstra/git/go-gin-app``` and save the change.

**Warning**: You may encounter this error:

```...driver failed programming external connectivity on endpoint ...```

Then read [Docker driver failed programming external connectivity on endpoint](https://www.codingnagger.com/2021/06/28/docker-driver-failed-programming-external-connectivity-on-endpoint/).

3. Once the workspace is ready, open the URL displayed in the terminal.
