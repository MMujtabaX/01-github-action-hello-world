# ⚙️ 01 — GitHub Actions: Hello World

![Workflow Status](https://github.com/MMujtabaX/01-github-action-hello-world/actions/workflows/main.yml/badge.svg)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?logo=githubactions&logoColor=white)

My first GitHub Actions workflow, and the starting point of a hands-on series on **CI/CD and DevOps automation**. The goal is to understand the anatomy of a workflow before building real pipelines.

## 🧩 Workflow Anatomy

Every GitHub Actions workflow follows the same structure:

```
name → event (on) → job → runner → steps
```

```yaml
name: Hello World Github Actions

on:
  push:
    branches: [main]        # Event: runs on every push to main

jobs:
  demo:                     # Job
    runs-on: ubuntu-latest  # Runner: a fresh Ubuntu VM hosted by GitHub
    steps:
      - name: Greetings     # Step
        run: echo "Hello World from Github Actions"
```

| Concept | Meaning |
|---------|---------|
| **Workflow** | A YAML file in `.github/workflows/` that defines an automated process |
| **Event** | What triggers the workflow, here a push to the `main` branch |
| **Job** | A group of steps that run on the same machine |
| **Runner** | The virtual machine that executes the job (`ubuntu-latest`) |
| **Step** | A single command or action inside a job |

## ▶️ See It Run

1. Push any commit to `main`.
2. Open the **Actions** tab of this repository.
3. Click the latest run, then the **demo** job, then **Greetings** to see the output:

```
Hello World from Github Actions
```

## 🎯 What I Learned

- Where workflow files live and how GitHub discovers them
- How events trigger workflows automatically
- How jobs run on GitHub-hosted runners
- How to read workflow logs in the Actions tab

## 🗺️ Series Roadmap

- [x] **01:** Hello World (this repo)
- [ ] Checking out code and running tests on push
- [ ] Linting and build checks on pull requests
- [ ] Using secrets and environment variables
- [ ] Deploying an application automatically

## 👤 Author

**Muhammad Mujtaba Khan Suri** — CS @ UBIT, University of Karachi
[GitHub](https://github.com/MMujtabaX)
