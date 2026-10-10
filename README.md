# Assembly: Endgame

A programming-themed word-guessing game built with **React** and **JavaScript**. Guess the hidden word before eight incorrect guesses eliminate the programming languages and leave only Assembly!

## Features

- **Interactive letter guessing:** Click letters on the on-screen keyboard to reveal the hidden word.
- **Eight incorrect attempts:** Each wrong guess eliminates one language, starting with HTML and ending with Ruby. Assembly is the last language standing.
- **Random words:** A new word is selected from the project's word list when a game starts or restarts.
- **Visual feedback:** Correct and incorrect guesses have different styles, and eliminated languages are crossed out.
- **Game status messages:** See a farewell message after an incorrect guess and a win or loss message when the game ends.
- **Win animation:** A confetti effect celebrates a completed word.
- **Play again:** Use the **New Game** button after winning or losing to begin another round.
- **Accessibility support:** Includes descriptive button labels and live status updates for screen readers.

## Technologies Used

| Technology | Purpose | Documentation |
| --- | --- | --- |
| React | Components and game state | [React docs](https://react.dev/) |
| JavaScript | Game logic and word selection | [JavaScript on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript) |
| Vite | Local development server and production builds | [Vite docs](https://vite.dev/) |
| clsx | Conditional CSS classes for game states | [clsx on npm](https://www.npmjs.com/package/clsx) |
| React Confetti | Celebration animation when you win | [react-confetti on npm](https://www.npmjs.com/package/react-confetti) |
| CSS | Layout, styling, and visual feedback | [CSS on MDN](https://developer.mozilla.org/en-US/docs/Web/CSS) |

The project also uses [React DOM](https://www.npmjs.com/package/react-dom) to render the application and [@vitejs/plugin-react](https://www.npmjs.com/package/@vitejs/plugin-react) to support React in Vite.

## Getting Started

### 1. Install prerequisites

Install [Node.js](https://nodejs.org/en/download) (which includes **npm**). Use a current, supported Node.js LTS version compatible with Vite.

To verify the installation, run:

```bash
node --version
npm --version
```

### 2. Download the project

Download and extract the project ZIP, or clone your GitHub repository. Open a terminal in the folder containing **`package.json`**.

### 3. Install dependencies

Run:

```bash
npm install
```

This installs all dependencies already listed in `package.json`. **You do not need to install each package separately.**

For reference, the project's direct dependencies are:

| Package | Version declared in `package.json` | Link |
| --- | --- | --- |
| `react` | `18.3.1` | [npm](https://www.npmjs.com/package/react) |
| `react-dom` | `18.3.1` | [npm](https://www.npmjs.com/package/react-dom) |
| `clsx` | `2.1.1` | [npm](https://www.npmjs.com/package/clsx) |
| `react-confetti` | `6.1.0` | [npm](https://www.npmjs.com/package/react-confetti) |
| `vite` | `latest` | [npm](https://www.npmjs.com/package/vite) |
| `@vitejs/plugin-react` (development dependency) | `*` | [npm](https://www.npmjs.com/package/@vitejs/plugin-react) |

If you were installing these packages **into a new project without this `package.json`**, the corresponding commands would be:

```bash
npm install react@18.3.1 react-dom@18.3.1 clsx@2.1.1 react-confetti@6.1.0 vite
npm install --save-dev @vitejs/plugin-react
```

For this repository, prefer the single `npm install` command above to use the declared dependencies.

### 4. Run the application

Start the development server:

```bash
npm run dev
```

Alternatively, the project also supports:

```bash
npm start
```

Open the local URL shown in the terminal (often `http://localhost:5173/`) in your browser.

### 5. Build for production (optional)

Create an optimized build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## How to Play

1. A random hidden word appears as blank letter spaces.
2. Click a letter on the on-screen keyboard to make a guess.
3. Correct letters are revealed wherever they appear in the word.
4. Each incorrect guess eliminates one programming language and displays a farewell message.
5. **Win** by guessing every letter before making eight wrong guesses, or **lose** after your eighth incorrect guess.
6. When the game ends, click **New Game** to get a new word and reset your guesses.

## Project Structure

```text
.
├── App.jsx           # Main game component, state, UI, and game-over logic
├── index.jsx         # React entry point
├── index.html        # HTML page and app mount point
├── index.css         # Application styles
├── languages.js      # Language names and chip colors
├── words.js          # List of words used for random selection
├── utils.js          # Random word and farewell message helpers
├── vite.config.js    # Vite configuration with React plugin
├── package.json      # Scripts and package dependencies
├── hint.md           # Original exercise hint
└── README.md         # Project documentation
```

## Available Commands

| Command | Description |
| --- | --- |
| `npm install` | Install project dependencies |
| `npm run dev` | Start the Vite development server |
| `npm start` | Start the Vite development server (alternate script) |
| `npm run build` | Generate a production build |
| `npm run preview` | Preview the production build |

## Project Background

This project was developed as a React learning exercise based on [Scrimba's Learn React course](https://scrimba.com/learn-react-c0e). It demonstrates React hooks, derived game state, conditional rendering, event handling, and reusable helper functions.
