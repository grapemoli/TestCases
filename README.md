# To Do
- test cases: learn how to write, and how to work
- printing in IDE: where to find the stdout

## Test Cases ... in Python!
e.g., let's look at the example test case
`self.assertEqual(say_hello("Qualified"), "Hello, Qualified!")`
The above compares the return of say_hello("Qualified") with "Hello, Qualified!" If the two are equal, then no errors are thrown.

### unittest 
_All Information Below is directly from: https://realpython.com/python-testing/_
The unittest library requires that:
1. You put your tests into classes as methods
2. You use a series of special assertion methods in the unittest.TestCase class instead of the built-in assert statement
i.e., use unittest

Before you dive into writing tests, you’ll want to first make a couple of decisions:
1. What do you want to test?
2. Are you writing a unit test or an integration test?

Then the structure of a test should loosely follow this workflow:
1. Create your inputs
2. Execute the code being tested, capturing the output
3. Compare the output with an expected result

The last step of writing a test is to validate the output against a known response. This is known as an **assertion**. There are some general best practices around how to write assertions:
- Make sure tests are repeatable and run your test multiple times to make sure it gives the same result every time
- Try and assert results that relate to your input data, such as checking that the result is the actual sum of values in the sum() example

#### Common Methods in unittest
The below are common methods and their equivalents:
.assertEqual(a, b) ... a == b
.assertTrue(x) ... bool(x) is True
.assertFalse(x)	... bool(x) is False
.assertIs(a, b)	... a is b
.assertIsNone(x) ... x is None
.assertIn(a, b) ... a in b
.assertIsInstance(a, b)	... isinstance(a, b)
*note: .assertIs(), .assertIsNone(), .assertIn(), and .assertIsInstance() all have opposite methods, named .assertIsNot(), and so forth *
