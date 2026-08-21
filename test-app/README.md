# Quiz CLI

## Project Overview

`Quiz CLI` is an interactive command-line quiz game built with Node.js. It loads quiz questions from a local JSON file, lets the user choose a category and question count, and then walks through a multiple-choice quiz with scoring, progress tracking, and end-of-quiz review feedback.

The application is designed as a small educational CLI for practicing JavaScript, Node.js fundamentals, and general programming concepts.

## Features

* Interactive terminal quiz experience.
* Category selection from a local question bank.
* Choice of quiz length, when enough questions are available.
* Randomized question order within each quiz session.
* Multiple-choice answers entered by number.
* Immediate correctness feedback after each question.
* Final score summary with a performance message.
* Review of incorrect answers at the end of the quiz.
* ANSI-colored terminal output for readability.

## Technologies and Tools

* Node.js `>=18.0.0`
* ES Modules (`"type": "module"` in `package.json`)
* Built-in Node.js modules:
  * `node:fs/promises`
  * `node:path`
  * `node:url`
  * `node:readline`
* JSON-based local content storage for quiz questions
* `node --test` script defined in `package.json`

## Project Structure

```text
test-app/
├── data/
│   └── questions.json
├── index.js
├── package.json
└── src/
    ├── colors.js
    ├── input.js
    └── quiz.js
```

### Key files and directories

* `index.js` — Main executable entry point for the CLI application.
* `package.json` — Project metadata, Node.js engine requirement, and npm scripts.
* `data/questions.json` — Quiz content organized into categories and questions.
* `src/colors.js` — ANSI color helpers for terminal formatting.
* `src/input.js` — Readline-based input helpers for prompts, selection, confirmation, and pause behavior.
* `src/quiz.js` — Core quiz logic, including question flow, scoring, progress display, and result summary.

## Setup Instructions

### Prerequisites

* Node.js `18.0.0` or newer
* npm-compatible Node.js environment

### Installation

This project does not declare any external npm dependencies. No installation step is required beyond having Node.js available.

If you want to verify the package metadata locally, you can inspect `package.json`, but there are no third-party packages to install from this repository.

### Configuration

No environment variables or external configuration files are required.

The quiz content is loaded from:

* `data/questions.json`

### Running the Application

```bash
npm start
```

You can also run the entry point directly:

```bash
node index.js
```

### Running Tests

A test script is defined in `package.json`:

```bash
npm test
```

At the time of inspection, no test files were present in the discovered repository tree, so the test command may not execute any tests unless test files are added.

## Getting Started

1. Clone the repository.
2. Change into the project directory.
3. Ensure Node.js `18+` is installed.
4. Run the application with `npm start`.
5. Choose a quiz category from the list.
6. Choose how many questions to answer.
7. Enter answers using the number shown beside each option.
8. Review your score and any incorrect answers at the end.
9. Choose whether to play again.

## Usage Examples

### Start the quiz

```bash
npm start
```

### Example interaction flow

```text
Choose a category:

  1. JavaScript Basics
  2. Node.js Fundamentals
  3. General Programming

How many questions?

  1. All questions
  2. 3 questions
  3. 5 questions

Your choice (enter number):
```

### Answering a question

```text
What keyword is used to declare a constant in JavaScript?

  1. var
  2. let
  3. const
  4. define

Your choice (enter number):
```

### End-of-quiz result summary

The application displays:

* total score
* percentage
* a performance message
* a review of incorrect answers, if any

## Architecture

The application is intentionally small and modular:

* `index.js` coordinates the application flow.
* `src/input.js` encapsulates terminal input handling.
* `src/quiz.js` contains the quiz state and game logic.
* `src/colors.js` centralizes terminal styling.
* `data/questions.json` acts as the local data source for quiz content.

This structure keeps presentation, input handling, and quiz logic separated while remaining simple enough for a CLI learning project.

## Development Notes

* The quiz uses built-in Node.js modules only; no external runtime libraries are required.
* Questions are stored locally, so the application does not depend on network access.
* The quiz engine shuffles questions for each run to vary the order of prompts.
* The CLI uses `readline` to collect user input interactively in the terminal.

## Limitations

* There is no persistent storage for scores or progress.
* There is no command-line argument support for selecting categories or question counts directly.
* The repository does not currently include automated test files, even though a test script is defined.