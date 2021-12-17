# Engine Test Data

This repository contains a single directory containing json files that can be used to test that any Flagsmith engine
written in a given language is correct. 

There are 2 JSON files in the directory: 

 * environment.json - contains the environment document as can be found in dynamo db
 * test_cases.json - contains a list of test cases; each test case contains the identity document and the corresponding response from the Django API.

To use this data, you will need to write a test case in the repository which contains the engine code and include 
this repository as a submodule to get access to the json files.

As an example, here are the steps to include the submodule and an example test in python. 

```
mkdir -p tests/engine_tests
cd tests/engine_tests
git submodule add git@github.com:Flagsmith/engine-test-data.git
```

Now, in the same directory, you can create your test, which in python (pytest), looks something like: 

```python
# TODO
```
