# Emotion Diary

[English](README.md) | [한국어](README.ko.md) | [日本語](README.ja.md)

A React and Vite web application for recording daily emotions, revisiting entries by month, and editing personal reflections over time.

[Open the live app](https://emotion-project-xi.vercel.app/)

![Emotion Diary home](image.png)

## Overview

Emotion Diary translates a real user's request for a simple emotional journal into a focused CRUD product. Each entry combines a date, one of five emotional states, and free-form text. Data stays in the browser through `localStorage`, so the app does not require an account or backend.

## Key features

- Create a diary entry with date, emotion, and text.
- Browse monthly entries.
- Sort entries from newest to oldest or oldest to newest.
- Open a detailed diary view.
- Edit or delete an existing entry.
- Persist entries across refreshes with browser `localStorage`.
- Handle unknown routes with a dedicated 404 page.
- Adapt the layout for desktop and mobile screens.

## Tech stack

- React 18
- Vite 6
- React Router DOM 7
- Context API and `useReducer`
- Browser `localStorage`
- CSS

## Project structure

```text
src/
  components/       Reusable editor, list, card, header, button, and emotion UI
  hooks/            Diary lookup and document-title hooks
  pages/            Home, create, edit, detail, and 404 routes
  util/             Emotion constants, image mapping, and date utilities
  App.jsx           Routing and global diary state
  main.jsx          Application entry point
```

## Run locally

```bash
git clone https://github.com/zxcc9867/Diary_App.git
cd Diary_App
npm install
npm run dev
```

Open `http://localhost:5173`.

## Build and preview

```bash
npm run lint
npm run build
npm run preview
```

## Data and privacy

All diary entries are stored only in the current browser's `localStorage`.

- There is no account system or cloud synchronization.
- Clearing browser storage removes the entries.
- Entries do not automatically move between devices or browsers.
- Do not use the current version for sensitive records on a shared device.

## Screens

### Home

<img src="image.png" width="800" alt="Emotion Diary home screen" />

### Edit

<img src="image-1.png" width="800" alt="Emotion Diary edit screen" />

## Possible next steps

- Emotion and keyword search.
- Monthly emotion statistics.
- Dark mode.
- Optional account-based cloud synchronization.
- Further mobile UX refinement.
