 # Netbox Metric Exporter (Work-in-progress)

___

## 🗒️ Table of Contents

1. [Project Overview & Goals](#-project-overview-&-goals)
2. [Project Summary](#-project-summary)
3. [Setup](#-setup)
4. [Installation](#-installation)
5. [Tools](#-tools)
6. [Data Retrieval & Inspection Process](#-data-retrieval-&-inspection-process)
7. [Development Phase](#-development-phase)
8. [Testing Phase](#-testing-phase)
9. [Deployment Phase](#-deployment-phase)
10. [Production](#-production)
11. [Grafana Visuals](#-grafana-visuals)
12. [Key Takeaways](#-key-takeaways)
13. [Findings & Insights](#-findings-&-insights)
14. [Future Improvements](#-future-improvements)
15. [References](#-references)

___ 

## Quote

“Take the leap of faith — the end results are worth the risk.” — Tania O.

## Note:

I am working on this in a Linux/Windows machine. Also, this might contains loads of information so please bear with me until I make this repository clean for user readability.

___

## Project Overview & Goals

___

## Project Summary

___

## Setup

### PyCharm

To start off, I utilized PyCharm as my desired IDE for this project and will be setting up a few packages to have this playground looking user-friendly and ready to use.

### Ubuntu WSL

I decided to have my terminal to be utilizing Ubuntu and I am working alongside with WSL (Windows Subsystem for Linux).

### GitLab

I created a GitLab account to have that DevOps environment and also being able to practice my CI/CD pipelines. I then needed this integrated with Pycharm so I can make commits and push them to the merge request.



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

<pre>uv init projectname</pre>
<pre>cd projectname</pre>
<pre>uv add ruff</pre>
<pre>uv run ruff check</pre>
<pre>uv lock</pre>
<pre>uv sync</pre>
<pre>uv tool install ruff</pre>
<pre>ruff --version</pre>

Python Install

<pre>uv python install</pre>

Creating a virtual environment:

<pre>uv venv</pre>

Install the locked requirements:

<pre>uv pip sync docs/requirements.txt</pre>

## Linters:

### Python Linters

- mypy
- pyright
- vulture
- pylint
  
### Python Unit Testing

- pytest
- unittest
  
### General & Cross-Language Linters

- yamllint
- hadolint
- markdownlint
  
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



___

## Development Phase

___

## Testing Phase

___

## Deployment Phase

___

## Production

___

## Grafana Visuals

___

## Key Takeaways

___

## Findings & Insights

___

## Future Improvements

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
[Ubuntu-WSL](https://ubuntu.com/desktop/wsl)
[UV-AstralDocs](https://docs.astral.sh/uv/)
[YAML](https://docs.gitlab.com/ci/yaml/)


___
