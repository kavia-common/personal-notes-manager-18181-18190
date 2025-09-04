# Notes Frontend (Astro)

This is a minimal, modern, light-themed notes manager built with Astro.

Features
- Create, read, update, delete notes (stored in localStorage for now)
- Search by title and content
- Tagging and filtering (AND filtering across multiple tags)
- Responsive layout with header, main grid (list + sidebar), and modal editor

Quick start
- npm install
- npm run dev (served at http://localhost:3000)
- Click "New" to create a note. Use search and tag filters on the right.

Structure
- src/layouts/Layout.astro: App shell, header, theme toggle, global styles
- src/components:
  - SearchBar.astro
  - FilterBar.astro
  - NoteList.astro (renders items, handles events)
  - NoteModal.astro (create/edit/view)
  - ThemeToggle.astro
- src/lib/storage.js: localStorage-backed CRUD and utilities

Future integration
- Replace src/lib/storage.js with API calls to the backend REST service.
- Keep the same public interfaces (listNotes, createNote, updateNote, deleteNote, getNote, searchNotes, getAllTags) to minimize refactors.
