# Simple Calculator Microservice

## Overview
This is a basic calculator microservice I built using Node.js and Express.  
It lets you do simple arithmetic operations like addition, subtraction, multiplication, and division through API endpoints.

## Prerequisites
Make sure you've got the following installed before you start:
- [Node.js](https://nodejs.org/en/download/)
- [npm](https://www.npmjs.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Git](https://git-scm.com/)

## How I Set It Up
1. **Created a project folder**:
   ```bash
   mkdir sit323-2025-prac4p
   cd sit323-2025-prac4p
   ```

2. **Initialised the Node project**:
   ```bash
   npm init -y
   ```

3. **Installed Express.js**:
   ```bash
   npm install express
   ```

4. **Built the server**:
   - Created an `index.js` file.
   - Added code to handle basic math operations using REST API.

5. **Wrote the documentation** (this README).

## How to Run It
- Open a terminal inside the project folder.
- Run the server with:
   ```bash
   node index.js
   ```
- It will start up at:
  ```
  http://localhost:3000
  ```

If successful, it’ll print:
```
Calculator microservice is running on port 3000
```

## API Endpoints
Each operation needs two query parameters: `num1` and `num2`.

Example in a browser:
```
http://localhost:3000/add?num1=5&num2=3
```

Expected JSON response:
```json
{
  "result": 8
}
```

## Error Handling
- If the numbers aren’t valid, the API throws a 400 error with a clear message.
- Division by zero is also handled properly.

Example error response if input is wrong:
```json
{
  "error": "Invalid input: num1 and num2 must be valid numbers."
}
```

Example error response if dividing by zero:
```json
{
  "error": "Division by zero is not allowed."
}
```

## Project Structure
```
sit323-2025-prac4p/
├── index.js
├── package.json
└── README.md
```

## How I Tested It
- Opened the endpoints directly in the browser.
- Also tested with Postman to double-check.
- Tried different inputs to see if errors were caught properly.

Example using curl:
```bash
curl "http://localhost:3000/multiply?num1=3&num2=4"
```
Response:
```json
{
  "result": 12
}
```

## GitHub Repository
Here’s the link to the GitHub repo where I pushed everything:
```
https://github.com/Sanindu-Rukshan/sit323-2025-prac4p.git
```

## Extra Notes
- The server only accepts numbers as input.
