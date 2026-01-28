# Task Completion Checklist

Run these commands before considering a task complete:

## 1. Linting (Always)

```bash
bin/rubocop -a
```

## 2. Tests (If code changed)

```bash
bin/rails test                 # Unit/integration tests
bin/rails test:system          # If UI changed
```

## 3. Security (If dependencies or sensitive code changed)

```bash
bin/brakeman --no-pager        # Static analysis
bin/bundler-audit              # Gem vulnerabilities
bin/importmap audit            # JS vulnerabilities
```

## 4. Full CI (Before PR/merge)

```bash
bin/ci
```

## Quick Validation Order

1. `bin/rubocop -a` - Fix style issues
2. `bin/rails test` - Run tests
3. `bin/brakeman --no-pager` - Security check

## CI Steps (from config/ci.rb)

1. Setup: `bin/setup --skip-server`
2. Style: `bin/rubocop`
3. Security: `bin/bundler-audit`
4. Security: `bin/importmap audit`
5. Security: `bin/brakeman --quiet --no-pager --exit-on-warn --exit-on-error`
6. Tests: `bin/rails test`
7. Seeds: `env RAILS_ENV=test bin/rails db:seed:replant`
