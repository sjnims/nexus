# Nexus Project Overview

## Purpose

A new Rails 8 application (freshly generated, minimal custom code yet).

## Tech Stack

- **Ruby**: 4.0.1
- **Rails**: 8.1.2
- **Database**: PostgreSQL
- **Web Server**: Puma (with Thruster for HTTP caching/compression)
- **Asset Pipeline**: Propshaft
- **JavaScript**: Importmap (no Node.js bundler)
- **CSS**: Dart SASS (dartsass-rails)
- **Frontend**: Hotwire (Turbo + Stimulus)
- **Background Jobs**: Solid Queue (database-backed)
- **Caching**: Solid Cache (database-backed)
- **WebSockets**: Solid Cable (database-backed)
- **Deployment**: Kamal (Docker-based)
- **Testing**: Minitest + Capybara + Selenium

## Key Dependencies

- `turbo-rails` - SPA-like page acceleration
- `stimulus-rails` - Modest JavaScript framework
- `jbuilder` - JSON API builder
- `image_processing` - Active Storage image variants
- `bootsnap` - Boot time optimization

## Security Tools

- `brakeman` - Static security analysis
- `bundler-audit` - Gem vulnerability scanning
