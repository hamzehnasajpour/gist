## CI/CD

* CI/CD is not one process. it's two distinct processes.
* CI is continuously integrating code back to main/master/trunk branch.
* CD (Continuous Delivery) is deploying that integrated code somewhere.

### Continuous Integration
* Automation process that allows developers to integrate their work into a repo.
* Helps to enable collabrative development across teams.
* Helps to identify integration bugs sooner.
* Teams can work in small chunks and regularly integrate new code into the main branch.

### Continuous Delivery
* Comes after CI process
* Prepares the code for release
* Automates the steps that are needed to deploy build

## DevOps steps
(1) Plan -> Code -> Build -> Test -> Release -> Deploy -> Operate -> (1)

CI: Code, Build and Test
CD: Release and Deploy

## CI/CD benefits
* Faster reaction times to changes
* Reduced code integration risk
* Higher code quality
* Code in version control works
* Less deployment time

* ** Different LOB applications within a company might use different CI/CD tools**
* It's OK to use different tools for CI/CD.
* It's important that processes are automated.
* There are many tools available for CI/CD

## IaC - Infrastructure as Code
* Describes your infrastructure in textual format for easy system configuration
* Textual code that you hand to an IaC tool to provision your infrastructure elements

Why?
* Reduces manual system and software configurations
* CMSs made this possible
* IaC makes it easy to rapidly provision the same platform repeatedly

### Approaches
1. Declarative
 * in a declarative approach, you specify the desired state
 * the tool determines how to get there

2. Imperative
 * in this approach, you specify the order of execuation
 * the tool executes commands in that order

### Benefits
* Faster time to production
* Faster, more efficient development
* Protection against staff churn
* Lower costs and improved use of developer time

### Tools
* Terraform
* Ansible
* Chef
* Puppet
* SaltStack

## CI
* is an automation process
* allows developers to integrate their work
* ensures that the software continues to work properly after being pushed
* enables collaborative development across teams
* helps idenify integration bugs sooner

### Main CI features
* short-lived branches 
  - reduces drift 
  - reduces parallel changes
* frequent pull requests 
  - frequent feedback from increased collaboration 
  - faster reaction to changes
  - reduced management risk
* automated ci tools
  
## Social Coding
* Opensource for inner source
  - Open source communities already did this
  - Enterprises are not doing this too
  - Developers used to work in privte repos
  - Code could not be reused
* All repositories are public
* Everyone is encouraged to contribute
* Anarchy is controlled via pull requests

### Steps
* Open: open an issue and assign it to yourself
* Discuss: Discuss new feature
* Fork
* Code
* Merge or Pull request

## CI Tools

### Jenkins
* Oldest of the three tools, implements both CI and CD
* Has a large ecosystem of plugins
* uses the 'Groovy' language in Jenkinsfile
* Enables developers to treat their CI/CD pipelines as code

### Circle CI
* Provided as a service, implements both CI and CD
* It allows you to treat your CI/CD pipeline as code (common theme)
* Uses circle.yaml file to control workflow

### Travis CI
* Provided as a service, implements both CI and CD
* Allows you to treat your CI/CD pipeline as code
* Uses a .travis.yml file to define workflow

### GitHub Actions
* is a CI/CD tool availables on every repo
* integrated into GitHub as a service
* allows you to treat your CI pipelines as code
* It uses a .github/workflows/ folder to store workflow definitions as .yaml files

Event > Runner > Jobs > Steps > Actions


## CD

A series of practices designed to ensure that code can be swiftly and safely deployed to production 
by delivering every change to a production-like environment.

### Goals
* main or master branch must always be deployable
* requires ckecks to ensure no bad code gets into main branch and breaks your product
* continuous integration runs test on every tpull request
* ensures things work before merging back to main branch

### Benefits
* Automate software transportation through SDLC stages
* Reduce deployment time
* Reduce costs
* Scale based on project size
* Deploy code automatically into each stage of SDLC

### Principles
* You need to build in quality
* You should work in small batches
* People should be problem-solving, not doing repetitive tasks
* You need to relentlessly pursue continuous improvment
* Everyone is responsible

### Best Practives
* Make every change releasable 
* Embrace trunk-based development
* Deliver through an automated pipeline
* Automate as many processes as possible
* Eliminate downtime
* Release at the granularity of test

### Deployment vs Delivery
* Continous Deployment can be part of a Continuous Delivery pipeline
* Continuos Delivery describes the automated movment of code through the SDLC
* Continuos Deployment is taking that code and deploying it to production
* The need for Continuous Deployment depends on business needs

### Tasks in CD piplelines
* Security scanning
* Vulnerability scanning
* Secret scanning
* Static Application Security Testing
* Dynamic Application Security Testing
* Deployment

### Tekton
* is a flixible, open source framework for creating CI/CD pipelines
* allows developers to build, test and deploy applications
* works across both cloud providers and on-premises systems

#### Conceptual Building Steps

Event > Trigger > Pipeline > Task > Step

#### Complete pipeline
* Checkout out the code
* Run quality checks
* Run unit tests
* Build container image
* Deploy to an environment
