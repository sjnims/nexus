# Codebase Structure

```text
nexus/
├── app/                      # Application code
│   ├── controllers/          # Request handlers
│   │   ├── concerns/         # Controller mixins
│   │   └── application_controller.rb
│   ├── models/               # ActiveRecord models
│   │   ├── concerns/         # Model mixins
│   │   └── application_record.rb
│   ├── views/                # ERB templates
│   │   ├── layouts/          # Layout templates
│   │   └── pwa/              # PWA manifest/service worker
│   ├── helpers/              # View helpers
│   ├── jobs/                 # Background jobs
│   ├── mailers/              # Email templates
│   ├── javascript/           # Stimulus controllers
│   │   └── controllers/      # JS controllers
│   └── assets/               # Static assets
│       ├── stylesheets/      # SCSS files
│       ├── images/           # Image files
│       └── builds/           # Compiled assets
├── config/                   # Configuration
│   ├── environments/         # Per-environment config
│   ├── initializers/         # Boot-time setup
│   ├── locales/              # I18n translations
│   ├── routes.rb             # URL routing
│   ├── database.yml          # Database config
│   ├── deploy.yml            # Kamal deployment
│   └── ci.rb                 # CI pipeline definition
├── db/                       # Database
│   ├── seeds.rb              # Seed data
│   ├── queue_schema.rb       # Solid Queue schema
│   ├── cache_schema.rb       # Solid Cache schema
│   └── cable_schema.rb       # Solid Cable schema
├── test/                     # Test files
│   ├── controllers/          # Controller tests
│   ├── models/               # Model tests
│   ├── integration/          # Integration tests
│   ├── helpers/              # Helper tests
│   ├── mailers/              # Mailer tests
│   └── fixtures/             # Test data
├── lib/                      # Library code
│   └── tasks/                # Rake tasks
├── bin/                      # Executables
├── public/                   # Static files served directly
├── .kamal/                   # Kamal deployment hooks
├── .github/                  # GitHub Actions
│   └── workflows/ci.yml      # CI workflow
├── vendor/                   # Vendored dependencies
├── Gemfile                   # Ruby dependencies
├── Gemfile.lock              # Locked versions
├── .rubocop.yml              # RuboCop config
├── .ruby-version             # Ruby version (4.0.1)
├── Dockerfile                # Container build
└── Procfile.dev              # Development processes
```

## Key Entry Points

- `config/routes.rb` - All URL routes
- `app/controllers/application_controller.rb` - Base controller
- `app/models/application_record.rb` - Base model
- `config/application.rb` - App configuration
