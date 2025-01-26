# Setting up a dev container for Go

* Primary author: [Bryson Hogsed](https://github.com/brysonth)

## Go Setup Tutorial

1. Prerequistes:
    1. Install Docker
    2. Install VSCode
    3. Install Git
2. Installation Steps
    1. Open up the terminal. Run the following commands:

        ```
        mkdir go_devcontainer
        ```

        ```
        cd go_devcontainer
        ```

        This makes a new directory

    2. Run this command:

        ```
        git init
        ```

        This initializes a Git repository in the directory that you just made

    3. Go to VSCode and open the repo you just created


    4. Create a directory called '.devcontainer'


    5. Create a file called 'devcontainer.json' inside of the '.devcontainer' directory


    6. Paste the following inside of the 'devcontainer.json' file:

    ```
    {
        "name": "Go Dev",
        "image": "mcr.microsoft.com/devcontainers/go:latest",
        "features": {
            "ghcr.io/devcontainers/features/docker-in-docker:1": {}
        },
        "postCreateCommand": "go version", 
        "customizations": {
            "vscode": {
                "settings": {},
                "extensions": [
                    "ms-go.go"
                ]
            }
        }
    }
    ```
    

        


    7. Open up the project in VSCode. Use "Ctrl + Shift + P" and click on "Dev Containers: Rebuild
       and Reopen in Container.


    8. In the src, create a file called "main.go" and copy this into it:

        package main

        import "fmt"

        func main() {
            fmt.Println("Hello COMP423")
        }


    9. Navigate to the terminal in VSCode.


    10. Run the command: go run main.go.

    
