# simple-bun

John Francis

9/16/2023

A simple project exploring the abilities of bun, the new javascript runtime.

This project will go into each of the abilities of bun at a very simple level.

# What is bun?
Bun is a:
- Runtime
- Package Manager
- Bundler
- Test Runner
- Package Runner
- API

# How to run bun on windows with vscode

As of now, bun doesn't have all it's functionality on windows, it's only just a runtime. Since I'm on windows, I decided to run bun from a docker container to get all the functionality. Here are 9 simple steps to run bun in a [docker](https://www.docker.com/) container using vscode:

1. Make sure you have the bun docker image installed. to do so, run `docker pull oven/bun`. Also make sure you have docker desktop open so that your container can run when it's ready.
2. Get the "[Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)" extension provided by vscode
3. In the bottom-left corner, click on the green symbol that kind of looks like this: [><]. 
4. There should be an option that says, "run in container," click on that.
5. Choose any container, we will soon change the settings.
6. A new directory should have been created called, ".devcontainer"
7. Go ahead and re-open the folder locally, exiting the container. (to do this, click on [><] and click on "reopen folder locally")
8. Now, we will change the settings. Go into .devcontainer/devcontainer.json, and edit it. Change the dev container name to "bun" and then image to "oven/bun". The json file will now look like this:
```json
{
	"name": "bun",
	// Or use a Dockerfile or Docker Compose file. More info: https://containers.dev/guide/dockerfile
	"image": "oven/bun"

  // ...
}
```

9. Now go to the [><] Button again and click "Reopen in Container." it will automatically open in the bun container. We can test it by going to a terminal and running `bun`. We should see:
```
Bun: a fast JavaScript runtime, package manager, bundler and test runner. (1.0.2)
```

# Easier way to do it:
1. create a new folder called .devcontainer
2. add a file called devcontainer.json
3. Add this to your file:
```json
{
  "name": "bun",
  "image": "oven/bun"
}
```

# What I did on this project
1. Ran `bun init` to initialize a project. It provided me with index.ts, package.json, and tsconfig.json. 

# Useful webistes:
- [Bun](https://bun.sh)
- [Bun quickstart](https://bun.sh/docs/quickstart)