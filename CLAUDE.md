# CLAUDE.md — NorCal Trackdays

## Project Overview

NorCal Trackdays is a new project for Northern California track day events. This repository is in its initial setup phase.

## Repository Status

This is a newly initialized repository. No application code, framework, or build tooling has been established yet.

## Development Guidelines

### Git Workflow

- **Default branch**: To be established (typically `main`)
- **Feature branches**: Use descriptive branch names prefixed with the feature area (e.g., `feature/event-registration`, `fix/calendar-display`)
- Commit messages should be concise and describe the "why" of the change
- Keep commits focused — one logical change per commit

### Code Quality

- Choose and configure a linter and formatter early (e.g., ESLint + Prettier for JS/TS projects)
- Write tests alongside new features
- Avoid committing secrets, credentials, or `.env` files — use `.gitignore`

### AI Assistant Notes

- Always read existing files before modifying them
- Do not create files unless necessary for the task at hand
- Prefer editing existing code over adding new files
- When the project stack is established, update this file with specific build commands, test commands, and architectural details
