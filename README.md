# Pennywise — Expense Tracker Mini Project

## Project pitch

**Pennywise helps students understand everyday spending.** Users can record income and expenses, group entries by category, review monthly totals, and compare spending with a budget. The project uses a familiar problem to explore how programming-language design and implementation choices affect a real application.

### Problem and audience

Small purchases are easy to forget, which makes it difficult to understand where money went. Pennywise is intended for students and first-time budgeters who want a simple, private way to keep track of spending.

### Core features

- Add income or expense entries with amount, category, description, and date.
- Review monthly balance, income, and expenses.
- Filter entries by category and delete entries.
- Set a monthly budget and view progress.
- Save entries in browser local storage.

## Connection to the PLP topics studied

### Reasons for studying programming-language concepts

Pennywise makes language concepts concrete. Its calculations, input handling, and interface show how a language's syntax, types, scope, and implementation environment affect correctness and maintainability.

### Programming domains and language evaluation criteria

This is a small **business / personal-finance information application**. For this domain, useful evaluation criteria include readability, reliability of calculations, ease of modification, and suitability for browser use. JavaScript is practical here because browsers execute it directly and it can update a web page interactively.

### Architecture, language categories, and design trade-offs

The application runs in a browser, so its design takes advantage of a user-facing environment with a DOM and local storage. JavaScript is a high-level, dynamically typed, multi-paradigm scripting language commonly used for web applications. Choosing it makes a browser-only project straightforward, while requiring care around input validation and type conversion. Keeping the prototype client-side also makes it easy to run, but means data is stored only in that browser.

### Implementation methods and programming environments

The browser is the programming environment for this project. The browser parses the HTML and CSS and executes the JavaScript using its JavaScript engine. This project does not implement its own compiler, interpreter, hybrid system, or preprocessor; those are implementation approaches studied in PLP and can be compared with the browser's language-processing pipeline. The file can be opened directly without a separate build step.

### Evolution of major languages

The project is written in JavaScript rather than pseudocode, C, C++, Python, or Java. In a presentation, compare how the same task—such as summing monthly expenses—would be expressed in pseudocode versus a general-purpose language. Then discuss how language evolution has expanded programming from lower-level machine-oriented work toward higher-level abstractions and managed, interactive environments. Do not claim Pennywise itself demonstrates all these languages.

### Syntax, expressions, ASTs, and parsing

The source contains JavaScript expressions for filtering transactions, summing amounts, formatting currency, and calculating budget progress. A language processor first recognizes lexical units (tokens), then uses grammatical rules to analyze structure; the resulting syntactic structure can be represented by an abstract syntax tree (AST). Top-down and bottom-up parsing are approaches for deriving that structure from a grammar. These are concepts used to explain how source code is processed; the application does not contain its own lexer, parser, or AST implementation.

### Names, bindings, and scopes

Names such as `transactions`, `budget`, `render`, and `current` are bound to values or functions. The app uses `const` for bindings that are not reassigned and `let` for values that change. Functions and event callbacks introduce scopes, and functions read or update application state through those bindings.

### Types, type checking, and conversions

JavaScript is dynamically typed, so values are not declared with fixed types in variable declarations. The form provides an amount as text-like input, and the app converts it with `Number(...)` before doing arithmetic. It checks that the result is finite and positive. This shows why conversions and validation matter. JavaScript is not a strongly statically typed language, so the pitch should describe this as an example to discuss type checking and strong typing, not as proof that the project enforces them.

## Short presentation pitch

“Hi, my mini project is Pennywise, a browser-based expense tracker for students. It lets a user record income and expenses, categorize transactions, see monthly totals, and compare spending with a budget. I chose a finance-tracking problem because it gives a practical setting for discussing programming-language concepts. The project uses JavaScript, a high-level, dynamically typed scripting language that runs in a browser. Its expressions calculate totals and filter data; its names and function scopes manage the application state; and its form handling demonstrates explicit type conversion and input validation. The browser processes the source code, which connects to our study of language implementation, syntax, and parsing. This prototype does not build a parser or demonstrate every language we studied, but it gives me a concrete example for comparing language features, design trade-offs, and implementation approaches.”

## Suggested demonstration

1. Explain the user problem and intended audience.
2. Show the balance, income, expense, and budget summaries.
3. Add an expense and point out the input conversion and validation in the code.
4. Filter transactions and explain the array expression and callback scope.
5. Explain that the browser runs the JavaScript and stores the data locally.
6. Connect the code to syntax, parsing, language categories, and evaluation criteria.

## Run it

Open `index.html` in a modern browser. The project code is organized into three files: `index.html` contains the page structure, `style.css` contains the design and responsive layout, and `script.js` contains transaction behavior, calculations, validation, and local storage. No installation or build step is required. The included GitHub Actions workflow publishes the site to GitHub Pages whenever changes are pushed to `main`. In the GitHub repository, enable Pages with **Settings → Pages → Build and deployment → GitHub Actions**. The first deployment will create the live site URL in the Actions run and Pages settings.

## Scope and limitations

This is an educational prototype. It stores data only in the current browser, does not connect to a bank, does not sync between devices, and is not financial advice. It is not an implementation of a programming language or parser.


