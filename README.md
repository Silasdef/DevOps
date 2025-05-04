📦 chocolatine.yml – GitHub Actions Workflow for Epitech Projects
🧠 Project Overview

This project provides a reusable GitHub Actions workflow designed to automate common tasks for Epitech coding projects. The goal is to enforce best practices and improve workflow efficiency by running automated checks on every push and pull request.
🚀 Features

    ✅ Runs on every push and pull request (except ignored branches or mirror repos)

    ✅ Checks coding style using Epitech’s official checker

    ✅ Compiles the project and verifies expected executables

    ✅ Runs unit tests with make tests_run

    ✅ Pushes the latest changes to a mirror repository via SSH

🔧 Technologies & Tools

    GitHub Actions (CI/CD)

    Docker containers:

        ghcr.io/epitech/coding-style-checker:latest

        epitechcontent/epitest-docker

    GitHub secrets for secure key management

🌐 Environment Variables

The following variables must be defined in the workflow:

    MIRROR_URL: SSH URL of the mirror repository

    EXECUTABLES: Comma-separated list of expected executables (e.g., bin/my_exec,test/test_exec)

🔐 Required Secrets

    GIT_SSH_PRIVATE_KEY: SSH private key used to push to the mirror repository

📁 File Location

The chocolatine.yml workflow file must be placed:

    Either at the root of your repository

    Or in the .github/workflows/ directory

📝 Usage

Copy the chocolatine.yml file into your repository and customize the environment variables as needed. The workflow will then automatically run on supported events.
📌 Notes

    Only the following external actions are allowed:

        actions/checkout

        pixta-dev/repository-mirroring-action

    The workflow is self-contained and should not depend on any other files.

    Hardcoded secrets are strictly forbidden — always use GitHub Secrets.
