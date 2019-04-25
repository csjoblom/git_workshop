class: middle, center

# Git, README's, and a little Docker

---

# Key points

This workshop will cover three topics:

* Key project files
* Git & Github
* Docker & Docker Compose

By the end of the workshop you will have the tools installed, forked a repo, and made a pull request.

---

# Requirements

Install:

* [Git](https://git-scm.com/downloads)
* [Docker CE](https://docs.docker.com/install/)
* [Docker Compose](https://docs.docker.com/compose/install/)

---

# Teams can be challenging

Why?

* Adding team members quickly becomes complex and time consuming
* Keeping everyone's copies of the code up-to-date
* Not losing other developer's work
* Being able to switch between tasks without losing work
* Supporting multiple operating systems

---

# REAMDE.md and LICENSE

`README.md` is the defacto standard place for important high-level information. `LICENSE` is the where people expect to find the license in OSS project. 

* Description of project
* Setup instructions
* Other information important
* H4C requires an MIT license

---

# Version Control

Version Control is universally used at software companies for good reason.

* Solves distributing and updating code
* Helps prevent losing code
* Tracks history of code
* Easy to switch between work
* VCS, Subversion, Mercurial, Team Foundation Server

---

# Git 

Working as a team requires being able to syncronize code accross team while still being able to work independently. Git allows every developer to have their own local copy of the codebase, maintain multiple sets of changes, and push code to the rest of the team.

* Very popular
* Used for Linux kernel development
* Distributed Version Control 

---

# GitHub

GitHub is a Git repository hosting platform that provides a web interface for managing the central repository.

GitHub:

* Very popular
* Used by a large number of OSS projects
* Provides good UI for code review 

---

# Docker

Most projects dependencies that must be setup when on-boarding contributors. Containerization tools, like Docker, and container oristration tools, like Docker Compose, allow projects to define their environment with code (Infrastructure as Code). 

Requires creating `Dockerfile` and `docker-compose.yaml`. See this files in this repo for a basic example.

---

# Workshop

We are going to:

* Fork the [Starting Projects Workshop repo](https://github.com/ryanrolds/starting_project_workshop)
* Checkout the fork
* Run the service with Docker & Docker Compose
* Create a branch
* Add your name to end of `README.md`
* Commit and push your change
* Create a pull request

---

# Fork Workshop Repo

Create a GitHub account if you don't already have one. Visit the [workshops repo on GitHub](https://github.com/ryanrolds/starting_project_workshop) and forfork the project.

---

# Checkout your fork

Open your command line (Git Bash on Windows). Creates a local copy of your fork.

``` bash
$ git clone https://github.com/<your username>/starting_project_workshop.git
Cloning into 'starting_project_workshop'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.
$ cd starting_project_workshop
```

---

<img src="/images/starting_projects_github.png"/>

---

# Start the service

Start the service:

``` bash
$ docker-compose up

```

Visit http://localhost:8080 in your browser, where you should find these slides.

---

# Create a branch in your repo

Creating branches is how you ensure your work is isolated and doesn't get deployed accidentally.

``` bash
$ git branch add_myself
$ git checkout add_myself
Switched to branch 'add_myself'
```

---

# Add name to README.md

Using your preferred editor, add your name to the end of `README.md`.

``` bash
$ tail README.md
```

---

# Status

Outputs status of repo

``` bash
$ git status
```

---

# Git Add

Add your modifiction to the next commit.

``` bash
$ git add README.md
```

---

# Git Commit

``` bash
$ git commit -m "Adding myself"
```

Shortcut: Skip add step if file isn't new

``` bash
$ git commit -m "Adding myself" README.md
```

---

# Push

``` bash
$ git push
```

---

# Submit PR

Visit your fork of the repo and create a PR.

---

# Questions? 

Ready?

---

# Tasks

* Fork https://github.com/ryanrolds/starting_project_workshop
* Checkout your fork
* Run and view the service with Docker & Docker Compose
* Create a branch
* Add your name to end of README
* Commit and push your change
* Create Pull Request to merge your branch to my (root) repo
