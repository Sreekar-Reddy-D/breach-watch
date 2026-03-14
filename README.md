# BreachWatch - Microservices Deployment 

This is the central deployment repository for **BreachWatch**, a secure password-checking application. It utilizes **Git Submodules** and **Docker Compose** to orchestrate the frontend and backend microservices into a single, cohesive local development environment.

## Live Demo
 Frontend: https://breachwatch-frontend.vercel.app

## Architecture

This repository links two separate codebases:
* **[breachwatch-frontend](https://github.com/Sreekar-Reddy-D/breachwatch-frontend):** A vanilla HTML/JS frontend served via an Nginx Alpine container.
* **[breachwatch-backend](https://github.com/Sreekar-Reddy-D/breachwatch-backend):** A Python Flask REST API running on a lightweight Python 3.10 slim container.

The services communicate over a custom, isolated Docker bridge network. 

## Quick Start (Local Development)

Because this repository uses Git Submodules to link the services, you must use the `--recursive` flag when cloning to pull all the code at once.

**1. Clone the repository**
```bash
git clone --recursive [https://github.com/Sreekar-Reddy-D/breach-watch.git](https://github.com/Sreekar-Reddy-D/breach-watch.git)
cd breach-watch
