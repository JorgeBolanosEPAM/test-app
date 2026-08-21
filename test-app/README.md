# test-app

## Project Description

`test-app` is an interactive Node.js command-line quiz application. It loads multiple-choice questions from a local JSON file, lets the user choose a quiz category and number of questions, tracks score and progress during the quiz, and presents a final review of incorrect answers.

The project is implemented as a small modular CLI application using modern JavaScript and Node.js ES modules.

## Key Features

- Interactive terminal-based quiz flow
- Category selection before starting a quiz
- Question count selection
- Randomized question order
- Multiple-choice answer input
- Immediate correctness feedback after each answer
- Progress indicator during the quiz
- Final score summary
- Performance message based on the final score
- Review of incorrect answers at the end of the quiz
- ANSI-colored terminal output for a better CLI experience

## Technologies and Tools

- JavaScript
- Node.js `>=18.0.0`
- ES Modules (`"type": "module"`)
- Built-in Node.js modules:
  - `node:fs/promises`
  - `node:path`
  - `node:url`
  - `node:readline`
- npm scripts:
  - `npm start`
  - `npm test`

No third-party npm dependencies are declared in `package.json`.

## Project Structure

```text
test-app/
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

### File and directory responsibilities

- `index.js` — Main executable entry point. Loads quiz data, shows the banner, and drives the application flow.
- `data/questions.json` — Local quiz content source containing the question categories and multiple-choice questions.
- `src/colors.js` — ANSI color and text-style helpers for terminal output.
- `src/input.js` — Readline-based input helpers for prompts, selection menus, confirmations, and pause actions.
- `src/quiz.js` — Core quiz logic implemented as the `Quiz` class.
- `package.json` — Project metadata and npm scripts.
- `README.md` — Project documentation.

## Setup Instructions

### Prerequisites

- Node.js `18.0.0` or newer
- npm-compatible environment

### Installation

No external package installation is required because the project does not declare third-party dependencies.

### Configuration

No environment variables or external configuration files are required.

Quiz content is loaded locally from:

- `data/questions.json`

### Running the Application

Start the quiz application with:

```bash
npm start
```

You can also run it directly with Node.js:

```bash
node index.js
```

## Getting Started

1. Clone the repository.
2. Change into the project directory.
3. Ensure Node.js `18.0.0` or newer is available.
4. Run the application:
   ```bash
   npm start
   ```
5. Follow the interactive prompts to:
   - choose a quiz category,
   - choose how many questions to answer,
   - select answers for each question,
   - review your final score and incorrect answers.
6. Optionally run the test script:
   ```bash
   npm test
   ```

## Usage Examples

### Start a quiz

```bash
npm start
```

### Run the application directly

```bash
node index.js
```

### Run the test suite

```bash
npm test
```

### Typical quiz flow

```text
1. Select a category
2. Choose the number of questions
3. Answer multiple-choice questions
4. Review your score and incorrect answers
5. Choose whether to play again
```

## Testing

The project defines a test script in `package.json`:

```bash
npm test
```

This runs Node.js built-in tests via:

```bash
node --test
```

No test files were identified in the repository structure provided.

## Architecture

The application is organized into a few small modules:

- `index.js` coordinates the application flow.
- `src/input.js` handles terminal input and user prompts.
- `src/quiz.js` contains the quiz engine and result review logic.
- `src/colors.js` centralizes terminal styling helpers.
- `data/questions.json` provides the quiz content consumed by the app.

This structure keeps the CLI entry point lightweight and separates UI, input handling, and quiz logic.

## Limitations

- Quiz content is fixed in the local `data/questions.json` file.
- The application does not use external APIs.
- No environment-based configuration is required or documented.
- No Docker, CI/CD, or deployment configuration was found in the repository.