# Runners and Dependencies

Almost always, a runner will need to checkout the code/data, install dependencies, and then proceed to other steps such as deployment, building, testing, etc. 

> Caching dependencies saves time and money if your Github repo is on a paid plan. 

## Declare a Runner

The first step in constructing a job is defining the runner. Syntax looks as follows:

To declare a runner, use the command: `runs-on: <runner>`.

## Installing Dependencies

Caching a dependency prevents jobs from multiple time consuming and expensive download steps. Dependencies usually do not change at a high enough frequency, so caching is typically safe to perform in most github actions. 


