<img width="638" alt="imadeveloper" src="https://github.com/richard-1257/alx-backend-python/assets/83041703/ba36a458-c7b7-498b-a6a2-4442471e2dda">

# Python - Async Comprehension
This project contains tasks for learning to use asynchronous comprehensions in Python 3.

## Tasks To Complete
+ [x] 0. **Async Generator**<br/>[0-async_generator.py](0-async_generator.py) contains an asynchronous coroutine called `async_generator` that takes no arguments and meets the following requirements:
  + The coroutine will loop 10 times, each time asynchronously wait 1 second, then yield a random number between 0 and 10.
  + Use the `random` module.

+ [x] 1. **Async Comprehensions**<br/>[1-async_comprehension.py](1-async_comprehension.py) contains a script that meets the following requirements:
  + Import `async_generator` from the previous task and then write a coroutine called `async_comprehension` that takes no arguments.
  + The coroutine will collect 10 random numbers using an async comprehensing over `async_generator`, then return the 10 random numbers.
