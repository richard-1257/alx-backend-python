![unit_test_vs_integration_test](https://github.com/richard-1257/alx-backend-python/assets/83041703/6279fb55-7b5e-4350-8016-c8d111093609)

# Unittests and Integration Tests
UnitTestsBack-endIntegration tests

- By Emmanuel Turlay, Staff Software Engineer at Cruise
- Weight: 1
Unit testing is the process of testing that a particular function returns expected results for different set of inputs. A unit test is supposed to test standard inputs and corner cases. A unit test should only test the logic defined inside the tested function. Most calls to additional functions should be mocked, especially if they make network or database calls.

The goal of a unit test is to answer the question: if everything defined outside this function works as expected, does this function work as expected?

Integration tests aim to test a code path end-to-end. In general, only low level functions that make external calls such as HTTP requests, file I/O, database I/O, etc. are mocked.

Integration tests will test interactions between every part of your code.

Execute your tests with
```python
$ python -m unittest path/to/test_file.py
```

## Resources
**Read or watch:**
- [unittest --- Unit testing framework](https://docs.python.org/3/library/unittest.html)
- [unittest.mock --- mock object library](https://docs.python.org/3/library/unittest.mock.html)
- [How to mock a readonly property with mock?](https://stackoverflow.com/questions/11836436/how-to-mock-a-readonly-property-with-mock)
- [parameterized](https://pypi.org/project/parameterized/)
- [Memoization](https://en.wikipedia.org/wiki/Memoization)

## Learning Objectives
- The difference between unit and integration tests.
- Common testing patterns such as mocking, parametrizations and fixtures

## Requirements
- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using `python3` (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly `#!/usr/bin/env python3`
- A `README.md` file, at the root of the folder of the project, is mandatory
- Your code should use the `pycodestyle` style (version 2.5)
- All your files must be executable
- All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
- All your classes should have a documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
- All your functions (inside and outside a class) should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
- A documentation is not a simple word, it's a real sentence explaining what's the purpose of the module, class or method (the length of it will be verified)
- All your functions and coroutines must be type-annotated.

## Required Files
**`utils.py`** ([or download](https://intranet-projects-files.s3.amazonaws.com/webstack/utils.py))<br/>Click to show/hide file contents


**`client.py`** ([or download](https://intranet-projects-files.s3.amazonaws.com/webstack/client.py))<br/>Click to show/hide file contents

**`fixtures.py`** ([or download](https://intranet-projects-files.s3.amazonaws.com/webstack/fixtures.py))<br/>Click to show/hide file contents

## Required Modules
- parameterized.

## Tasks To Complete
+ [x] 0. **Parameterize a unit test**<br/>[test_utils.py](https://github.com/richard-1257/alx-backend-python/blob/master/0x03-Unittests_and_integration_tests/test_utils.py) contains a python module that meets the following requirements:
  + Familiarize yourself with the `utils.access_nested_map` function and understand its purpose. Play with it in the Python console to make sure you understand.
  + In this task you will write the first unit test for `utils.access_nested_map`.
  + Create a `TestAccessNestedMap` class that inherits from `unittest.TestCase`.
  + Implement the `TestAccessNestedMap.test_access_nested_map` method to test that the method returns what it is supposed to.
  + Decorate the method with `@parameterized.expand` to test the function for following inputs:
    ```python
    nested_map={"a": 1}, path=("a",)
    nested_map={"a": {"b": 2}}, path=("a",)
    nested_map={"a": {"b": 2}}, path=("a", "b")
    ``` 
  + For each of these inputs, test with `assertEqual` that the function returns the expected result.
  + The body of the test method should not be longer than 2 lines.


