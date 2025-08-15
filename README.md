 # Netbox Metric Exporter (Work-in-progress) ** Day 3 and we just getting started.. **

___

## 🗒️ Table of Contents

1. [Project Overview & Goals](#-project-overview-&-goals)
2. [Project Summary](#-project-summary)
3. [What is the MVC Framework](#-what-is-the-mvc-framework)
4. [Setup](#-setup)
5. [Installation](#-installation)
6. [Tools](#-tools)
7. [Data Retrieval & Inspection Process](#-data-retrieval-&-inspection-process)
8. [Development Phase](#-development-phase)
9. [Testing Phase](#-testing-phase)
10. [Deployment Phase](#-deployment-phase)
11. [Production](#-production)
12. [Grafana Visuals](#-grafana-visuals)
13. [Key Takeaways](#-key-takeaways)
14. [Findings & Insights](#-findings-&-insights)
15. [Future Improvements](#-future-improvements)
16. [References](#-references)

___ 

## Quote

“Take the leap of faith — the end results are worth the risk.” — Tania O.

## Note:

I am working on this in a Linux/Windows machine. Also, this might contains loads of information so please bear with me until I make this repository clean for user readability.

___

## Project Overview & Goals



___

## Project Summary


## What is the MVC Framework

The Model, View, Controller Framework is a software design pattern that organizes an application into three main components: Model, View, and Controller. 

Model: 
- Represents the blueprint or layout of the framework.

View: 
- Represents the UI (User Interface) / presentation layer.

Controller:
- Represents the middle-man, the way it interacts with the Model and View components.

___

## Setup

### PyCharm

To start off, I utilized PyCharm as my desired IDE for this project and will be setting up a few packages to have this playground looking user-friendly and ready to use.

### Ubuntu WSL

I decided to have my terminal to be utilizing Ubuntu and I am working alongside with WSL (Windows Subsystem for Linux).

### GitLab

I created a GitLab account to have that DevOps environment and also being able to practice my CI/CD pipelines. I then needed this integrated with Pycharm so I can make commits and push them to the merge request.

Below, is a list of what I did to make GitLab interact with the PyCharm IDE.

1. Generate a SSH key
2. Generate a GitLab PAT (Personal Access Token)
3. Setup Git in PyCharm
4. Add GitLab Account to PyCharm
5. Clone a Repository
7. Commit, Push, and Pull

### Installation 

### Oh My Zsh

I wanted my terminal to look great using Oh My Zsh. 

First, I installed it:

<pre>sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"</pre>

Then, I wanted a theme so, I decided to go with agnoster however, you need to install a Powerline-patched font in order to work properly:

If you are running a Debian or Ubuntu-based Linux distribution:

<pre>sudo apt-get install fonts-powerline</pre>

Now, I can change the theme to Agnoster

<pre>nano ~/.zshrc</pre>

Find this line:

<pre>ZSH_THEME="robbyrussell"</pre>

Change it to:

<pre>ZSH_THEME="agnoster"</pre>

Then, save (CTRL + O, Enter) and exit (CTRL + X).

Reloading the shell:

<pre>source ~/.zshrc</pre>

### UV

I installed UV, a fast Python package and project manager written in Rust. This package manager works like the speed of lighting and is useful to get the packages needed for this DevOps project.

To install UV:

<pre>curl -LsSf https://astral.sh/uv/install.sh | sh</pre>

Projects

<pre>uv init projectname</pre> # Initialize the project
<pre>cd projectname</pre>      # Change directory to the project
<pre>uv add ruff</pre>         # Add ruff, a python linter
<pre>uv run ruff check</pre>   # Ruff's action to analyze your code for issues
<pre>uv lock</pre>             # Lock file to manage your python dependencies
<pre>uv sync</pre>             # Synchronize your python environment
<pre>ruff --version</pre>      # Will display the version of the Ruff installed 

Python Install

<pre>uv python install</pre>

Creating a virtual environment:

<pre>uv venv</pre>

Install the locked requirements:

<pre>uv pip sync docs/requirements.txt</pre>

## Linters:

### Python Linters

- `uv add mypy`  # Static type checker
- `uv add pyright` # Fast type checking, optimized for larger projects
- `uv add vulture` # Finds unused code
- `uv add pylint`  # Code style and error checking (classic linter)
  
### Python Unit Testing

- `uv add pytest` # Third-party testing framework; uses simple assert statements, automatically discovers tests, more flexible and minimal boilerplate.
- `uv run pytest` # Run tests
- `unittest` # Built-in Python testing framework; uses classes and self.assert*() methods.
  
### General & Cross-Language Linters

- `uv add yamllint` # Is a linter for YAML files — it checks your YAML for syntax errors, formatting issues, and style consistency.
- `uv add hadolint` # Is a linter for Dockerfiles — it checks your Dockerfile for syntax errors, best practices, and security issues.
- `uv add markdownlint` # Is a linter for Markdown files — it checks .md files for style, formatting, and best practices.

___

## Tools

- Docker: Runs applications in lightweight, portable containers.
- FastAPI: High-performance Python framework for building APIs.
- GitLab: Web-based Git repository manager with CI/CD pipelines.
- Grafana: Visualizes metrics and logs from various data sources.
- Harbor: Cloud-native container registry for storing and managing images.
- KubeSphere: Enterprise-grade container management platform built on Kubernetes with multi-tenant, CI/CD, monitoring, and observability features.
- Netbox: IP address management (IPAM) and data center infrastructure management (DCIM) tool.
- Postman: API development platform for testing and documenting endpoints.
- Prometheus: Open-source monitoring system that collects metrics and alerts on events.
- Python: High-level programming lanaguage for general-purpose and scripting tasks.
- Ubuntu (WSL): Linux operating system running inside Windows via the Windows Subsystem for Linux.
- YAML: Human-readable data serialization format often used for configuration files.

___

## Data Retrieval & Inspection Process

In this section of the project, I utilized Postman, the preferred API platform, to conduct GET requests to API endpoints and receive response payloads.

___

## Development Phase

I utilized Netbox Cloud, Prometheus Client, FastAPI, and Python to create the MVC framework. This is all taken place in local development on my laptop. I gathered...

___

## Testing Phase

Tested my code with unittests and made sure what I was pushing to production had passed those tests smoothly and by following CI/CD best practices.
By making clean and concise code that is readable and passing all linters. Linters and unittests have different code quality. 

___

## Deployment Phase

The Python code is containerized with Docker and image is securely managed and stored into Harbor. From there, it is deployed into KubeSphere Then, the data will be visualized using Grafana to display the ....

Procedures:

1) Build docker image 
2) Push docker image to Harbor, which is a registry where something like a docker image would live
3) Configured project into KMGT and have it set up to pull the docker image from harbor. 
4) Spin up the Kubernetes pods in KMGT.

___

## Production

I utilized Thanos query to verify the exporter is exposing all the metrics needed to be able to create Grafana Visualizations.

___

## Grafana Visuals

Created Grafana Visualizations with the scrapejob.yml files. 
___

## Key Takeaways

___

## Findings & Insights

___

## Future Improvements

I will create alert monitoring mechanisms....

___

## References 

[Docker](https://www.docker.com/)

[FastAPI](https://fastapi.tiangolo.com/)

[GitLab](https://about.gitlab.com/)

[Grafana](https://grafana.com/)

[Harbor](https://goharbor.io/)

[KubeSphere](https://kubesphere.io/)

[Netbox](https://netboxlabs.com/)

[Postman](https://www.postman.com/)

[Prometheus](https://prometheus.io/)

[Python](https://www.python.org/)

[Pycharm](https://www.jetbrains.com/pycharm/)

[Oh My Zsh](https://ohmyz.sh/)

[Installing Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

[Oh My Zsh Themes](https://github.com/ohmyzsh/ohmyzsh/wiki/themes)

[GitLab-CI-YAML](https://docs.gitlab.com/ci/yaml/)

[Netbox-RestAPIs](https://netboxlabs.com/docs/netbox/integrations/rest-api/)

[Ubuntu-WSL](https://ubuntu.com/desktop/wsl)

[UV-AstralDocs](https://docs.astral.sh/uv/)

[YAML](https://docs.gitlab.com/ci/yaml/)


___
