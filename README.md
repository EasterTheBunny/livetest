# Live Test
Thank you for taking a look at our code test. It shouldn't take very long and is
designed to give us a feel for how you would solve common problems that we
encounter on a regular basis.

We don't want this test to take you very long so you are free to use any
language and framework you are most comfortable in.

Step 1: Fork this repo.
Step 2: Continue with the 3 part test and submit your new fork when you are done.

## Part 1 - API
Create a web application API with a single endpoint, `/sort`.

### The endpoint *MUST*:
- respond only to POST and produce 403 for everything else
- produce a json result with correct mime headers
- take json data in a request body with the following `input format`
- group input data by code
- produce a sorted result with the following `output format`

#### Input Format
```json
[
  {
    "id": 99999,
    "category": 18,
    "code": "SIMPLE_CODE",
    "description": "Some short description",
    "amount": 12.34
  },
  {
    "id": 22222,
    "category": 17,
    "code": "SIMPLE_CODE",
    "description": "Some short description",
    "amount": 43.21
  },
  {
    "id": 33333,
    "category": 18,
    "code": "OTHER_CODE",
    "description": "Some short description",
    "amount": 123.45
  }
]
```

#### Output Format
```json
{
  "SIMPLE_CODE": [
    {
      "id": 99999,
      "category": 18,
      "description": "Some short description",
      "amount": 12.34
    },
    {
      "id": 22222,
      "category": 17,
      "description": "Some short description",
      "amount": 43.21
    }
  ],
  "OTHER_CODE": [
    {
      "id": 33333,
      "category": 18,
      "description": "Some short description",
      "amount": 123.45
    }
  ]
}
```

### The endpoint *MAY* (extra optional challenge):
- offer other grouping options via input parameters such as by category
- offer filtering options
- offer sorting options for the grouped items

If you would like to generate random data to test your API endpoint,
[try this](https://www.generatedata.com/). It's what we'll also be using to
generate test data.

## Part 2 - Unit Testing
Many modern web frameworks and even languages have unit testing built in. Please
use this feature to add unit tests to your API.

## Part 3 - Documentation
We love documentation. Please include some basic docs in markdown of your API
endpoint. If you do the optional challenge, you'll need to make some decisions
about input parameter format, but then you'll also need to describe it to us!

## Bonus Points!!
### Automation
We love automated build/test tools. If you know anything on the lines of Docker
or your favorite brand of CI/CD tools, feel free to add in some automation.

### Details Matter
We tend to work in an environment with many people that all have an individual
opinion on how to write and format code. However, the flame wars over tabs and
spaces can get out of hand. So we just tend to agree on one style and all stick
to it for our own sanity and peace. If you have any thoughts on this subject,
feel free to add some simple style guides. We use `editorconfig`, for example,
but do what you like.
