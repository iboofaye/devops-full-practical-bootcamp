# devops-full-practical-bootcamp

# DevOps Full Practical Bootcamp Project 

# Goal
Throughout the project, we will explore various aspects of DevOps, including application development, containerization with Docker, creating CI/CD pipelines, managing Kubernetes clusters, and implementing effective monitoring practices.
<br> To Establish a Robust and Reliable Development process by settting version control using Git, implementing comprehensive Unit Tests, and setting up effective workflows to ensure that only properly tested code is merged from other branches into the Master branch.

## Requirements

Git clone initial code from this Github Repo - [https://github.com/iboofaye/devops-full-practical-bootcamp](https://github.com/iboofaye/devops-full-practical-bootcamp/tree/initial_starter_code)
```
git clone git@github.com:iboofaye/devops-full-practical-bootcamp.git
```

## Step 1 - Get the inital start code onto your system
## Step 2 - Add Unit Tests
## Step 3 - Create a workflow

1.) Create a directory called .github/workflows within the directory containing .git
2.) And create a workflow ‘YAML’ file, let's call it ci_cd_wf.yml
3.) Git add and push changes (This automatically invokes the Git actions and sets up the CI/CD Pipeline which on push to the master branch)

```
name : test

on:
  push:
    branches:
      - main

jobs:
  test:
    runs-on : ubuntu-latest

    steps:
      - name: Check out repo code
        uses: actions/checkout@v3

      - name: Setup Python
        uses: actions/setup-python@v3
        with:
          python-version: "3.x"

      - name: Install Dependencies
        run: |
          python -m pip install -r requirements.txt
      - name: Run tests
        run: |
          python -m pytest calculator.py
```

## Step 4 - Check our Gitflow with a new branch

## Step 5 - Fix all the errors to make a successful build

## Step 6 - 
## Step 7 - 
## Step 8 - 
## Step 9 - 
## Step 10 - 

### As the the project comes to a close, it's important to reflect on the progress made so far.

## Future Scope Recommendations - 
<br> Now that the initial code is in place, it's time to focus on improving its quality. One way to do this is to add more checks such as linters, code coverage, and code quality checks. </br>
<br> Another recommended step is to add 'runs on' actions like a pull request. This allows for a more streamlined workflow and can help ensure that the code changes are thoroughly tested before being merged into the main branch. </br>

## Appendix
<br> This repository has three branches -
### 'main' branch contains the file code for the project
### 'initial_starter_code' contains the inital code to start with
### 'test' - The state of the project with a wrong test added for reference - this is supposed to fail the merge to master process in our workflow
</br>
