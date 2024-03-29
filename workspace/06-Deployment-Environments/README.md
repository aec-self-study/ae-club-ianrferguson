# Deployment Environments

## What are they?

* The version of a project that customers / users interact with == production
* Developers make changes in a separate environment (e.g., a new branch) before merging with the production branch

## Typical Workflow

* Write and test code in development environment
* Open PR + stage the code for testing
* Deploy to the production environment

## Continuous Integration

* CI = process of automating code changes from multiple contributors in a single project
* This validates a dev change before it's merged, which gives you confidence that there will not be unexpected conflicts upstream
