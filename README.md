# Quiz CLI

## Project Overview

`Quiz CLI` is an interactive Node.js command-line quiz application located in the `test-app/` directory. It runs entirely in the terminal and lets a user:

- choose a quiz category
- choose how many questions to answer
- respond to multiple-choice questions by number
- see immediate correctness feedback
- track score and progress
- review missed answers at the end

The quiz content is loaded from a local JSON file, so the application does not require network access or external services.

## Features

- Interactive terminal quiz experience
- Category-based question selection
- Variable quiz length based on available questions
- Randomized question order
- Multiple-choice answers entered by number
- Immediate correct/incorrect feedback
- Progress display during the quiz
- Final score, percentage, and performance summary
- Review of incorrect answers after completion
- ANSI-colored terminal output
- Local JSON-driven quiz content

## Technologies and Tools

- **Node.js** `>=18.0.0`
- **JavaScript** with **ES Modules** (`"type": "module"`)
- **npm** scripts
- Built-in Node.js modules:
  - `node:fs/promises`
  - `node:path`
  - `node:url`
  - `node:readline`
- Local JSON data storage for quiz questions
- Terminal/ANSI color formatting implemented in the application code

## Project Structure

```text
prueba2/
└── test-app/
    ├── README.md
    ├── data/
    │   └── questions.json
    ├── index.js
    ├── package.json
    └── src/
        ├── colors.js
        ├── input.js
        └── quiz.js
```

### Important files and directories

- `test-app/index.js` — main entry point for the CLI application
- `test-app/src/input.js` — terminal input helpers built on `readline`
- `test-app/src/quiz.js` — quiz state, scoring, progress, and result logic
- `test-app/src/colors.js` — ANSI color and formatting helpers
- `test-app/data/questions.json` — quiz categories and question data
- `test-app/package.json` — package metadata and npm scripts
- `test-app/README.md` — existing project documentation inside the app directory

## Setup Instructions

### Prerequisites

- Node.js `>=18.0.0`
- A terminal capable of running interactive CLI applications

### Installation

The application does not declare any external npm dependencies. From the repository root, move into the app directory:

```bash
cd test-app
```

If you want npm to initialize local metadata such as a lockfile, you can run:

```bash
npm install
```

This project does not require third-party packages for normal use.

### Configuration

No environment variables or external configuration files are required.

Quiz content is stored locally in:

```text
test-app/data/questions.json
```

## How to Run the Project

From the `test-app/` directory, start the quiz with:

```bash
npm start
```

You can also run the entry point directly:

```bash
node index.js
```

## Getting Started

1. Clone the repository.
2. Open a terminal and change into the application directory:

   ```bash
   cd test-app
   ```

3. Ensure you are using Node.js `>=18.0.0`.
4. Start the application:

   ```bash
   npm start
   ```

5. Follow the prompts to:
   - choose a category
   - choose a question count
   - answer each multiple-choice question
6. Review your final score and any missed answers.
7. Choose whether to play again when prompted.

## Usage Examples

### Start the quiz

```bash
cd test-app
npm start
```

### Run the entry point directly

```bash
node index.js
```

### Typical quiz flow

The application will guide you through an interactive session where you:

- select a quiz category
- choose how many questions to answer
- enter the number of your chosen answer for each question
- receive immediate feedback
- see your final score and a review of incorrect answers

## Testing

The package defines a test script:

```bash
npm test
```

This runs:

```bash
node --test
```

No separate test files were present in the accessible repository tree, so this command may not execute any tests until tests are added.

## Build

There is no build step defined for this project.

## Known Limitations

- No automated tests were present in the discovered repository tree
- No Docker configuration is included
- No CI/CD workflow files were discovered
- No environment-based configuration is required or supported
- The application is designed for terminal use only

## Notes

- The quiz data is local and the application does not require internet access.
- The project is implemented as a single-package CLI app inside `test-app/`.
- The repository uses only built-in Node.js capabilities and local source files.
