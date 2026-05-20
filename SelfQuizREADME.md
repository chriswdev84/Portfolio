# Self-Quiz App

[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![Vue.js](https://img.shields.io/badge/Vue.js-3.0+-green.svg)](https://vuejs.org/)
[![Vite](https://img.shields.io/badge/Vite-4.0+-blue.svg)](https://vitejs.dev/)

## Overview

The Self-Quiz App is a browser-based logic puzzle built with Vue 3 and Vite. It generates self-referential quiz questions and lets users interactively answer them while the app validates consistency and correctness.

## Screenshots

<a href="screenshots/PuzzleStart.png"><img src="screenshots/PuzzleStart.png" width="300" alt="Puzzle Start"></a>
<a href="screenshots/PuzzleEnd.png"><img src="screenshots/PuzzleEnd.png" width="300" alt="Puzzle End"></a>

## Why this project?

This project started because the only self-referential logic puzzle I found was a daily game on LogiQuiz. I liked playing it, but I wanted more than one puzzle per day, so I built this app to generate additional self-referential logic quizzes on demand.

## Features

- **Self-referential questions**: Each quiz item can reference other statements, creating a logic puzzle experience.
- **Interactive UI**: Built with Vue 3 for a fast, reactive single-page experience.
- **Immediate feedback**: The app checks answers as users interact.
- **Modern frontend stack**: Uses Vite for fast builds and development.

## How to use

1. Start the app locally.
2. Read each quiz statement and choose the truth values.
3. Submit your answers and use the app’s feedback to learn which logic paths are correct.

## Prerequisites

- Node.js 18 or later
- npm 9 or later

Verify your installation:

```bash
node -v
npm -v
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/chriswdev84/self-quiz
cd self-quiz
```

2. Install dependencies:

```bash
npm install
```

## Running the application

Start the development server:

```bash
npm run dev
```

Open the local URL shown in the terminal to view the app.

## Build and preview

Build for production:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## Project structure

- **index.html**: Application entry HTML.
- **package.json**: Project dependencies and scripts.
- **vite.config.ts**: Vite configuration.
- **run-app.bat**: Windows launch helper.
- **src/main.ts**: Vue application bootstrap.
- **src/App.vue**: Root component and UI layout.
- **src/quizGenerator.ts**: Quiz generation and validation logic.
- **src/style.css**: Styling for the application.
- **tsconfig.json**: TypeScript compiler configuration.
- **tsconfig.app.json**: App-specific TypeScript settings.
- **tsconfig.node.json**: Node-specific TypeScript settings.

## Scripts

- `npm run dev`: Start development server
- `npm run build`: Build production bundle
- `npm run preview`: Preview the production build