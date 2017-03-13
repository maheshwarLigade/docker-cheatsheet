# docker-cheatsheet
Docker cheatsheet.
##What is Docker?
Docker is an open-source project that automates the deployment of applications inside software containers.

This is the simple cheatsheet of docker. It contains some of the basic commands which I used generally.

###Installing Docker :-
I download and used docker on my osx.
<a href="https://docs.docker.com/engine/installation/#platform-support-matrix">Download Docker </a>

###Basic Docker Commands :-
List of running Process <br/>

```docker ps```

###List images:<br/>

```docker images```
###List all processes that were ever run

```docker ps -a ```

###List only the container IDs:
```docker ps -a -q```

###Running processes:
 ```docker run <image>
 
docker run -d <image> = run in disconnected / daemon mode

docker run --name="Some Name" = name the running instance

docker start <name> = will restart a closed / exited instance of the image

docker exec -it <name> <command> = run a command within a running container without changing the state of the running container

docker stop <name> = stop a running container by using the name
```



There are many other options of docker commands that will help you to.

####Options:

 ``` --config string      Location of client config files (default "/Users/username/.docker")
 
  -D, --debug              Enable debug mode
  
      --help               Print usage
      
  -H, --host list          Daemon socket(s) to connect to (default [])
  
  -l, --log-level string   Set the logging level ("debug", "info", "warn", "error", "fatal") (default "info")
  
      --tls                Use TLS; implied by --tlsverify
      
      --tlscacert string   Trust certs signed only by this CA (default "/Users/username/.docker/ca.pem")
      
      --tlscert string     Path to TLS certificate file (default "/Users/username/.docker/cert.pem")
      
      --tlskey string      Path to TLS key file (default "/Users/username/.docker/key.pem")
      
      --tlsverify          Use TLS and verify the remote
      
  -v, --version            Print version information and quit```
  
  
####Management Commands:
  >checkpoint  Manage checkpoints
  >container   Manage containers
  >image       Manage images
  >network     Manage networks
  >node        Manage Swarm nodes
  >plugin      Manage plugins
  >secret      Manage Docker secrets
  >service     Manage services
  >stack       Manage Docker stacks
  >swarm       Manage Swarm
  >system      Manage Docker
  >volume      Manage volumes ```

####Commands:
 ``` <p>attach      Attach to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  deploy      Deploy a new stack or update an existing stack
  diff        Inspect changes on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes</p> ```
  
  
###  Cleaning up Docker:

 ```docker rm containerid = removes an instance of the container that was run
 
docker rm `docker ps -a -q` = remove all stopped containers

docker rmi image-name = removes the docker image and its dependencies ```


###Port redirection in docker

```docker run -P = will redirect the container's port to a random port on the host machine's user port (port no 32,000+)

docker run -p 8080:82 = will redirect the container's port 82 to a port 8080 on the host machine's user port 

docker port <container-name> = will list the port mapping information```


There are the many other things that we need to know, but as a developer this are the some basic thing you should must know.
If you know please let me know.

