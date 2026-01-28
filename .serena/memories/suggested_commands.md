# Suggested Commands

## Development Server

```bash
bin/dev              # Start server + CSS watcher (uses Procfile.dev)
bin/rails server     # Rails server only (port 3000)
```

## Database

```bash
bin/rails db:create          # Create databases
bin/rails db:migrate         # Run migrations
bin/rails db:seed            # Seed data
bin/rails db:reset           # Drop, create, migrate, seed
bin/rails db:test:prepare    # Prepare test database
```

## Testing

```bash
bin/rails test               # Run all unit/integration tests
bin/rails test:system        # Run system tests (browser)
bin/rails test test/models   # Run specific directory
bin/rails test test/models/user_test.rb:42  # Run specific test
```

## Code Quality

```bash
bin/rubocop          # Lint Ruby code
bin/rubocop -a       # Auto-fix issues
bin/brakeman         # Security static analysis
bin/bundler-audit    # Gem vulnerability check
bin/importmap audit  # JS dependency audit

# Format non-Ruby files
npx prettier --write "**/*.{md,json,yml,yaml,js,css,scss}"

# Lint markdown
npx markdownlint-cli2 "**/*.md" --fix
```

## Full CI Suite

```bash
bin/ci               # Run complete CI pipeline locally
```

## Rails Console & Generators

```bash
bin/rails console           # Interactive console
bin/rails generate model    # Generate model
bin/rails generate controller  # Generate controller
bin/rails routes            # Show all routes
```

## Assets

```bash
bin/rails dartsass:build   # Compile SCSS once
bin/rails dartsass:watch   # Watch and compile SCSS
bin/importmap pin <pkg>    # Add JS dependency
```

## Deployment (Kamal)

```bash
bin/kamal setup      # Initial server setup
bin/kamal deploy     # Deploy application
bin/kamal rollback   # Rollback deployment
```

## System Utilities (macOS/Darwin)

```bash
git status/add/commit/push   # Version control
ls -la                       # List files
cd /path                     # Change directory
rm -f file                   # Remove file (always use -f)
```
