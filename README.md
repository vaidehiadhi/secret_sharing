
# Project Title

# Shamir's Secret Sharing Implementation

This project implements a simplified version of Shamir's Secret Sharing algorithm in JavaScript. It reconstructs a secret (the constant term of a polynomial) given a set of points on that polynomial.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [File Structure](#file-structure)
- [Error Handling](#error-handling)
- [Limitations](#limitations)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

- Node.js (version 10.4.0 or later for BigInt support)

## Installation

1. Clone this repository or download the source code.
2. Navigate to the project directory in your terminal.

## Usage

1. Prepare your input data in JSON format. Two example files (`testcase1.json` and `testcase2.json`) are provided.
2. Run the script using Node.js:

   ```
   node secret_sharing.js
   ```

3. The program will output the secret (constant term) for each test case.

## How It Works

The script performs the following steps:

1. Reads and parses the JSON input files.
2. Extracts the points from the parsed data.
3. Uses Lagrange interpolation to reconstruct the polynomial.
4. Calculates the constant term (y-intercept) of the polynomial, which is the secret.

## File Structure

- `secret_sharing.js`: The main script containing the implementation.
- `testcase1.json`: First test case input file.
- `testcase2.json`: Second test case input file.

## Error Handling

The script includes basic error handling for file reading and insufficient data points. If an error occurs, it will be logged to the console.

## Limitations

- This implementation uses JavaScript's BigInt for handling large numbers. Ensure your Node.js version supports BigInt (10.4.0 or later).
- The script assumes well-formed JSON input. Malformed input may cause unexpected behavior.

## License

This project is open source and available under the [MIT License](LICENSE).