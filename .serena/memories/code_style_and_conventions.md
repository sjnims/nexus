# Code Style and Conventions

## Ruby Style

- Uses **rubocop-rails-omakase** (Rails default style guide)
- Config: `.rubocop.yml` inherits from omakase gem
- Run `bin/rubocop -a` to auto-fix issues

## Naming Conventions (Rails Standard)

- **Models**: Singular, CamelCase (`User`, `BlogPost`)
- **Controllers**: Plural, CamelCase + Controller (`UsersController`)
- **Tables**: Plural, snake_case (`users`, `blog_posts`)
- **Files**: snake_case matching class name (`user.rb`, `users_controller.rb`)
- **Methods**: snake_case (`find_by_email`)
- **Constants**: SCREAMING_SNAKE_CASE

## File Organization

```text
app/
  controllers/    # Request handlers
  models/         # ActiveRecord models
  views/          # ERB templates
  helpers/        # View helpers
  jobs/           # Background jobs (Solid Queue)
  mailers/        # Email templates
  javascript/     # Stimulus controllers
  assets/         # CSS, images
```

## JavaScript

- Importmap-based (no npm/webpack)
- Stimulus for interactivity
- Turbo for SPA-like navigation
- Controllers in `app/javascript/controllers/`

## CSS

- Dart SASS (`.scss` files)
- Main file: `app/assets/stylesheets/application.scss`

## Testing

- Minitest (Rails default)
- Fixtures in `test/fixtures/`
- System tests with Capybara + Selenium
