# TDD 

* **Code with confidence**
* TDD -> 92% high quality code
* Improve maintainability
* **You can only test what you know**


## Design principles for Apollo
* Use a high level language
* Divide into jobs
* Restart on failure
* Checkpoint good state
* Hardware monitors the software
* Send telemetry

## Levels:
1. unit tests
2. integration tests (BDD)
3. system tests
4. acceptance tests

## BDD (outside in)
* Focuses on the behaviour of the system from the outside
* Works great for integration tests

## TDD (inside out)
* Focuses on the system works from the inside
* tests drive the design
* first tests then write the codes and make the tests pass

### TDD Workflow
1. Fail - Red (write a test case that fails)
2. Pass - Green (write code to make it pass)
3. Blue - Refactor (improve the code quality) --> 1

## test paths
* happy path: verify that a function returns positive outcomes when expected
* sad path: verify that a function responds to exceptions appropriately and without breaking

## Test fixtures
* create an initial testing state
* run tests in isolation
* ensure repeatable results

### usecases
* preparation of input data
* setup/creation of fake or mock objects
* loading a db with known set of data
* copying a specific know set of files

### Test fixtures operate at three levels of specificity: 
* Module 
* Test case 
* Test 

### order
1. setup: module -> class -> case
2. tearDown: case -> class -> module

## Factories and Fakes
* are useful for creating and maintaining a large amount of test data.
* Factories generate fakes with realsitic test data
* Fakes behave like real objects during testing, so developers test fakes like they test real data.

## Mocking 
* is a process for creating objects that mimic the behavior of real objects.

### when we use mock
* have an external service that is not under test
* need to change the behavior of a dependent system under test
* dont have a remote connection to another component

### Types
1. Patch: patches a function call
2. Mock and MagicMock Object 
  * mocks an entire object
  * best used as a return value
