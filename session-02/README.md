# React.js and Next.js Mastering Course

## Session 02

### 1. Styling Frameworks and Libraries

- Frameworks and Libraries
- [Bootstrap](https://getbootstrap.com/) vs [TailwindCSS](https://tailwindcss.com/)
- UI Components vs Utility Classes

### 2. Version Controlling

- Introduction VCS
- VCS Providers ([Github](https://github.com), [GitLab](https://gitlab.com), [Bitbucket](https://bitbucket.com))

### 3. JavaScript Basics

- Java vs JavaScript
  - Java is an OOP programming language while Java Script is an OOP scripting language. Java creates applications that run in a virtual machine or browser while JavaScript code is run on a browser only
- How similar is Java and JavaScript?
  - JavaScript is a beginner-friendly programming language that allows developers to design interactive websites.
  - On the other hand, Java is a complex language used to build sophisticated applications like Android apps, chatbots, and financial software
- Is JavaScript influenced by Java?
  - JavaScript has no direct relation to Java besides being used for web technologies. The name choice was a marketing move to encourage adoption.
- ECMAScript (ES)
  - [ECMA International](https://ecma-international.org/) (formally European Computer Manufacturers Association) is a non-profit organization that develops standards in computer hardware, communications, and programming languages.
  - On the web it is famous for being the organization which maintain the `ECMA-262` specification
- Why was it called JavaScript?
  - In the beginning, the ECMAScript was called `Mocha`.
  - It was later changed as `LiveScript`, Netscape changed the name to `JavaScript` so they could position it as a companion for the Java language, a product of their partner, Sun Microsystems.
  - Apart from some superficial syntactic similarities, though, JavaScript is in no way related to the Java programming language.
- ECMAScript (ES) Versions

  - `ECMAScript 1` was released in `1997`
  - Most Popular ECMAScript version is `ES6` released in 2015. This version introduced several important features such as:
    - `Let` and `Const`
    - Arrow Functions
    - Template Literals
    - Classes
    - Destructuring
    - Default Parameters
    - Maps
    - Sets
  - ECMAScript 2016 `(ES7)`
  - ECMAScript 2024 `(ES15)` is the latest version
  - [Versions](https://webreference.com/javascript/basics/versions/)

- Event Loop

  The **Event Loop** is a core concept in JavaScript, especially in environments like browsers and Node.js. JavaScript is single-threaded, meaning it can execute only one task at a time. However, it can handle asynchronous operations (like timers, network requests, or user interactions) without blocking the main thread.

  The event loop works with the **call stack** and the **callback queue**:

  - The **call stack** is where JavaScript keeps track of function calls and executes them one by one.
  - The **callback queue** holds messages (callbacks) from asynchronous operations that are ready to be executed.

  The event loop constantly checks if the call stack is empty. If it is, it takes the first callback from the queue and pushes it onto the stack for execution. This process allows JavaScript to perform non-blocking operations and remain responsive.

  **Example:**

  ```js
  console.log("Start");

  setTimeout(() => {
    console.log("Timeout callback");
  }, 0);

  console.log("End");
  ```

  **Output:**

  ```
  Start
  End
  Timeout callback
  ```

  Even though the timeout is set to 0, the callback runs after the synchronous code, demonstrating how the event loop handles asynchronous tasks.

- Other Single Threaded Languages

  While JavaScript is well-known for its single-threaded nature, there are other programming languages that also operate primarily on a single thread by default:

  - **Python**: The standard implementation (CPython) uses a Global Interpreter Lock (GIL), which means only one thread executes Python bytecode at a time, making it effectively single-threaded for CPU-bound tasks.
  - **Lua**: Lua runs in a single thread unless explicitly extended with libraries for concurrency.
  - **Ruby (MRI)**: The main Ruby interpreter (MRI) also uses a GIL, so only one thread runs Ruby code at a time.
  - **PHP**: Each request is handled in a single thread or process; PHP scripts themselves are single-threaded unless using extensions.
  - **Swift (Playgrounds)**: Swift code in Playgrounds runs on a single thread unless concurrency is explicitly introduced.

  These languages can still perform asynchronous or concurrent operations using event loops, external libraries, or by spawning separate processes, but their default execution model is single-threaded, similar to JavaScript.

- Embedded JavaScript

- JavaScript Variable Types
  - Number
  - String
  - Boolean
  - Null
  - Undefined
  - BigInt
  - Symbol
  - Object
  - Array

## 4. Basic Git Commands

Git is a distributed version control system that helps you track and manage changes to your code. Follow these steps to set up a Git repository and push your code to a remote service like GitHub.

### 1. Initialize a Git Repository

In your project directory, initialize a new Git repository:

```bash
git init
```

### 2. Add Files to the Staging Area

Stage all changes by running:

```bash
git add .
```

Or add individual files:

```bash
git add path/to/your/file
```

### 3. Commit Your Changes

After staging your files, create a commit with a descriptive message:

```bash
git commit -m "Initial commit"
```

### 4. Add a Remote Repository

Link your local repository to a remote repository:

```bash
git remote add origin https://github.com/your-username/your-repo.git
```

```bash
git remote -v
```

### 5. Push to the Remote Repository

Push your commits to the remote repository’s main branch:

```bash
git push -u origin main
```

Adjust the branch name if you're using a different branch.

### 6. Check the Status of Your Repository

To see the current state of your working directory and staging area, use:

```bash
git status
```

**Explanation:**  
This command shows which files have been modified, staged, or are untracked. It's useful for reviewing changes before committing or pushing to a remote repository.

### 6. Clone the Remote Repository

To copy a remote repository to your local machine, use the `git clone` command:

```bash
git clone https://github.com/your-username/your-repo.git
```

**Explanation:**  
This command downloads the entire repository, including its history, to your computer. Replace the URL with the actual address of the repository you want to clone.
