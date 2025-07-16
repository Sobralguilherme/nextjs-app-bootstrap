# Login System App - Technical Documentation

## 1. Introduction
This is a Ruby on Rails application that implements a user authentication system including login, logout, and registration functionalities. The system features a custom frontend built with HTML, CSS, and JavaScript, and uses PostgreSQL as the production database (SQLite in development). It includes tests using RSpec (or Minitest as an alternative), scaffold generation, and RESTful routes. The project also includes a complete Docker setup for containerized deployment.

## 2. Requirements
- Ruby 3.2.3
- Rails 8.0.2
- Node.js and Yarn (for JavaScript dependencies)
- SQLite3 (for development)
- PostgreSQL (for production)
- Docker and Docker Compose (optional, for containerized setup)

## 3. Installation Instructions

### Running Locally (without Docker)
1. Clone the repository:
   ```bash
   git clone <repo-link>
   cd login_system_app
   ```
2. Install Ruby gems:
   ```bash
   bundle install
   ```
3. Install JavaScript dependencies:
   ```bash
   yarn install
   ```
4. Setup the database:
   ```bash
   rails db:create db:migrate db:seed
   ```
5. Start the Rails server:
   ```bash
   rails server
   ```
6. Access the app at `http://localhost:3000`

### Running with Docker
1. Ensure Docker and Docker Compose are installed.
2. Build and start the containers:
   ```bash
   docker-compose up --build
   ```
3. Access the app at the configured Docker host and port.

## 4. Running Tests
- Run the test suite with:
  ```bash
  bundle exec rspec
  ```
  or if using Minitest:
  ```bash
  rails test
  ```

## 5. Project Structure
- `app/controllers/` - Controllers handling HTTP requests.
- `app/models/` - ActiveRecord models representing database tables.
- `app/views/` - HTML templates for rendering views.
- `app/assets/` - CSS, JavaScript, and image assets.
- `config/` - Application configuration files.
- `db/` - Database migrations, schema, and seeds.
- `bin/` - Executable scripts including `rails`, `setup`, and `dev`.
- `test/` or `spec/` - Test files.
- `Dockerfile` and `docker-compose.yml` - Docker configuration files.

## 6. Useful Commands
- `bundle install` - Install Ruby dependencies.
- `yarn install` - Install JavaScript dependencies.
- `rails db:create` - Create the database.
- `rails db:migrate` - Run database migrations.
- `rails db:seed` - Seed the database with initial data.
- `rails server` or `bin/dev` - Start the development server.
- `bin/setup` - Setup script to install dependencies, prepare database, and start server.
- `rails console` - Open Rails console.
- `bundle exec rspec` or `rails test` - Run tests.

## 7. Available API Endpoints
- `GET /login` - Login page.
- `POST /login` - Authenticate user.
- `DELETE /logout` - Logout user.
- `GET /signup` - Registration page.
- `POST /signup` - Create new user.
- Other RESTful routes for user management as scaffolded.

## 8. Environment Configuration
- `.env` file (if used) to store environment variables such as database credentials, secret keys, etc.
- `config/database.yml` configures database connections for development, test, and production.
- `config/environments/` contains environment-specific settings.

## 9. Full Command List to Run the Project from Scratch
```bash
# Clone the project
git clone <repo-link>

# Enter project directory
cd login_system_app

# Install Ruby dependencies
bundle install

# Install JavaScript dependencies
yarn install

# Setup the database
rails db:create db:migrate db:seed

# Start the Rails server
rails server
```

## Development Workflow
- Analyze requirements and design features.
- Document specifications and plan implementation.
- Implement features using Rails MVC architecture.
- Write tests to cover functionality.
- Maintain and refactor code as needed.

---

This documentation provides a comprehensive overview to help developers understand, run, and maintain the login system app effectively.
