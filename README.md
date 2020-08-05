# Most Answered Jurisdiction

Filters records from a MonQcle API (through v4) by matching a question and value. Generates a summary with the name of the jurisdiction that has the most matches.

Part of a code test completed 8/4/2020 by Nick Steele for MonQcle.

## Prerequisites

* Node.js

> Don't have Node.js? [Download](https://nodejs.org/en/download/) it for your operating system.

## Installation

`npm i -g`

...now you can call it from the command line using `most-answered-jurisdiction`

## Creating binaries

`npm run build`

...will produce 3 executables, one for each target: Linux, MacOS and Windows. Now there is nothing to install!

> Want to kow more about building node.js binaries? See [Pkg](https://github.com/vercel/pkg#readme)

## Usage

> most-answered-jurisdiction -host \<host> -question-type \<question-type> -value \<value>

---

| Parameter     	| Description                      	                           |
|---------------	|----------------------------------	                           |
| host          	| A valid MonQcle hostname i.e. "http://ec2-204-236-247-13.compute-1.amazonaws.com/previewer/57aa20d9d6c9e79438a8019e/get_json"    	                           |
| question-type 	| The question type, i.e. "Categorical - mutually exclusive"   |
| value         	| The value you're filtering, i.e. "Yes"                       |


---

## Example

Request...
```bash
most-answered-jurisdiction -host http://ec2-204-236-247-13.compute-1.amazonaws.com/previewer/57aa20d9d6c9e79438a8019e/get_json --question-type "Categorical - mutually exclusive" --value "Yes"
```

Response...
```bash
Jurisdiction Name: New Jersey
Total: 14
Took: 0.859 seconds

Done
```

## Response in detail

The **Jurisdiction Name**
_is the name of the jurisdiction that has the most question answered with the type and answer value specified._

The **Total**
_is how many times the jurisdiction contained an answer with the type and answer value specified._

**Took**
_is how many seconds elapsed to provide the result._
