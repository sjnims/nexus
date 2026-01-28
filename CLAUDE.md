# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with
code in this repository.

## Commands

```bash
# Development server (Rails + SASS watcher)
bin/dev

# Run all tests
bin/rails test

# Run single test file or specific line
bin/rails test test/models/user_test.rb
bin/rails test test/models/user_test.rb:42

# Run system tests (browser)
bin/rails test:system

# Lint and auto-fix
bin/rubocop -a

# Format markdown, JSON, YAML, JS, CSS
npx prettier --write "**/*.{md,json,yml,yaml,js,css,scss}"

# Lint markdown
npx markdownlint-cli2 "**/*.md" --fix

# Security checks
bin/brakeman --no-pager
bin/bundler-audit
bin/importmap audit

# Full CI pipeline locally
bin/ci

# Database
bin/rails db:migrate
bin/rails db:test:prepare
```

## Architecture

Rails 8.1 application using the Hotwire stack:

- **Turbo** for SPA-like navigation without JavaScript
- **Stimulus** for JS interactivity (`app/javascript/controllers/`)
- **Importmap** for JS dependencies (no Node.js bundler)
- **Dart SASS** for stylesheets (`app/assets/stylesheets/`)
- **Propshaft** as asset pipeline

Database-backed infrastructure (no Redis required):

- **Solid Queue** for background jobs
- **Solid Cache** for caching
- **Solid Cable** for WebSockets

Deployment via **Kamal** (Docker-based, config in `config/deploy.yml`).

## Style

Uses `rubocop-rails-omakase` (Rails default style).
Run `bin/rubocop -a` before committing.
