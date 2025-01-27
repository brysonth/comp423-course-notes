# Setting up a dev container for Go

* Primary author: [Bryson Hogsed](https://github.com/brysonth)
* Reviewer: [Nate Hicks](https://github.com/hicksnat)

## Go Setup Tutorial

1. Prerequistes:
    1. Install Docker
    2. Install VSCode
    3. Install Git
2. Installation Steps
    1. Open up the terminal. Run the following commands:

        `
        mkdir go_devcontainer
        `

        `
        cd go_devcontainer
        `

        This makes a new directory

    2. Run this command:

        `
        git init
        `

        This initializes a Git repository in the directory that you just made

    3. Go to VSCode and open the repo you just created


    4. Create a directory called '.devcontainer'


    5. Create a file called 'devcontainer.json' inside of the '.devcontainer' directory


    6. Paste the following inside of the 'devcontainer.json' file:

        `
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
        `
    
    

        


    7. Open up the project in VSCode. Use "Ctrl + Shift + P" and click on "Dev Containers: Rebuild
       and Reopen in Container.


    8. Create a directory called src. In the src, create a file called "main.go" and copy this into it:

    `
    
        package main

        import "fmt"

        func main() {
            fmt.Println("Hello COMP423")
        }

    `

    9. Navigate to the terminal in VSCode. cd into the src directory.


    10. Run the command: go run main.go.


    <!-- I was able to run through the tutorial and do my hello world! Overall it's good. 
    There were like 2 improvements I noticed
    1. Whenever you put something in code with the three ticks ```, it resets the counter for your
    numbered bullet points. So it ends up looking a little weird on the website. it doesn't do this if
    you just use `<code>`
    2. This is kind of the opposite problem, but the .devlog paste code gets formatted on the website so
    that it's not properly formatted when the reader copy and pastes it. So I had to do some extra 
    looking around myself how to format it
    3. My src file and main.go file weren't there when I opened it in the dev container, so you might
    just want to include something about creating it if not
    4. Similar to yours, I also had to cd into the src file, so maybe mention that-->
