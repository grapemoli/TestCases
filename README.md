# To Do
- test cases: learn how to write, and how to work
- printing in IDE: where to find the stdout

## Test Cases ... in Python!
e.g., let's look at the example test case
`self.assertEqual(say_hello("Qualified"), "Hello, Qualified!")`
The above compares the return of say_hello("Qualified") with "Hello, Qualified!" If the two are equal, then no errors are thrown.

### unittest 
_All Information Below is directly from: [https://realpython.com/python-testing/]_
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

# Markdown Help
Note that all information is taken from the Qualified Markdown Guide: [www.qualified.io]

## Basic Features
You can *italicize* or **bold.** You can also ~~strikethrough.~~

There are ordered lists:
1. one
2. two 
3. three

There are also unordered lists:
* one
* two
* three
- one
- two
- three

Feel free to nest the lists as you'd like.

## Tables
| Name | Description          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |


## Code Formatting
### Inline Formats
Inline formatting is done using single backticks to format text in a special monospace format. For example, on line four, `say_hello()` should actually be `**sayHello()**`.

### Multiple Lines
You use triple backticks to format text as its own distinct block.

```
class Grace() {
  private:
    std::string name;
    int age;
  public:
    Grace();
    std::string getName();
    int getAge();
    void setAge(int age);
    void setName(std::string name);
};
```

## JSON Customization
Note that this is unique to Qualified.
```%method-doc
{  
  "method": "intersect_arrays",
  "desc": "Combines the values within two arrays which are the same.",
  "args": {
    "arrA": {
      "type": "Array<Integer>"
    },
    "arrB": {
      "type": "Array<Integer>"
    }
  },
  "constraints": [
    "`0 <= arrA.length <= 10`",
    "`arrA` and `arrB` are never null"
  ],
  "returns": {
    "type": "Array<Integer>",
    "desc": "An intersected array that contains only the elements within both arrA and arrB"
  },
  "examples": [
    {
      "args": [[1,2,3], [2,3,4]],
      "returns": [2,3]
    },
    {
      "args": [[1,2,3, 6, 8, 9, 12], [1,2]],
      "returns": [1,2]
    }
  ]
}
```
