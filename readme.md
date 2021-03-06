cli-args-parser-kata
===
The goal of this program is to model a cli arguments parser. Given a series of input the program should produce a valid output according to the following specification.

## Before you start
- Try not to read ahead, do one task at a time (the trick is to learn to work incrementally)!
- Make sure you only test for correct inputs;
- You may use whatever programming language you prefer;
- You should commit your code on GitHub or any other SCM repository you prefer;
- You should release your work under an OSI-approved open-source license of your choice;
- Remember to sent a PR once you're done with the kata 😉

## Specification
Choose one of the following input formats:
- string like arguments `"--foo bar"`
- array like arguments `["--foo", "bar"]`

### 1. parse a `simple` flags
  given the following input:
  ```sh
  --foo
  ```
  the program should produce either a dictionary or a JSON object as follows:
  ```JSON
  {"foo": true}
  ```

### 2. parse a `composite` flags
  given the following input:
  ```sh
  --foo bar
  ```
  the program should produce either a dictionary or a JSON object as follows:
  ```JSON
  {"foo": "bar"}
  ```

### 3. parse a `composite` flags with integer values
  given the following input:
  ```sh
  --number 1
  ```
  the program should produce either a dictionary or a JSON object as follows:
  ```JSON
  {"number": 1}
  ```

### 4. parse multiple flags at once
  given the following input:
  ```sh
  --foo --bar baz --number 1
  ```
  the program should produce either a dictionary or a JSON object as follows:
  ```JSON
  {"bar": "baz", "foo": true, "number": 1}
  ```

### 5. handle multiple values for the same flag
  given the following input:
  ```sh
  --foo --bar baz --bar zab --number 1
  ```
  the program should produce either a dictionary or a JSON object as follows:
  ```JSON
  {"bar": ["baz", "zab"], "foo": true, "number": 1}
  ```

### 6. try to support both `string` and `array` input formats
within the same function or a new function one of your choice.


## General requirements
- **We would love to see your submission written in JavaScript**. Although, you can use whatever language and frameworks you want. Use something that you know well.
- **Provide a README with instructions** on how to compile and run the application.

**IMPORTANT:**  Implement the requirements focusing on **writing the best code** you can produce.

**CODE SUBMISSION:** Add the code to your own Github account and send us the link.

Credits to [Ivo Putzer](https://github.com/ivoputzer) for the original idea.
