SIMON WAS HERE
<br>

This repository serves as a template for setting up a modern Drupal 10 project using Composer for package management and integrating Symfony components. By leveraging Symfony's features, you can enhance your Drupal development experience and create a more modular architecture.

## Table of Contents

- [Requirements](#requirements)
- [Getting Started](#getting-started)
  - [1. Clone the Repository](#1-clone-the-repository)
  - [2. Navigate to Project Directory](#2-navigate-to-project-directory)
  - [3. Install Dependencies](#3-install-dependencies)
  - [4. Configure Database Connection](#4-configure-database-connection)
  - [5. Start the Development Server](#5-start-the-development-server)
- [Managing Modules and Packages](#managing-modules-and-packages)
- [Finding Modules](#finding-modules)
- [Contributing](#contributing)
- [License](#license)

## Requirements

Before you begin, ensure you have the following prerequisites:

- [Composer](https://getcomposer.org/download/)
- [Symfony CLI](https://symfony.com/download)

## Getting Started

Follow these steps to set up your project locally:

### 1. Clone the Repository

Start by cloning this repository to your local development environment using either SSH or HTTPS:

#### SSH:
  ```
  git clone git@github.com:santiagotrindade/drupal-basicsite-project.git
  ```

#### HTTPS:
  ```
  git clone https://github.com/santiagotrindade/drupal-basicsite-project.git
  ```

### 2. Navigate to Project Directory:

Change your working directory to the newly cloned repository:

   ```
   cd drupal-basicsite-project
   ```

### 3. Install Dependencies:

Use Composer to install the project dependencies:
   ```
   composer install
   ```

### 4. Configure Database Connection

  - Create the Database: Make sure to create the database you've specified in the settings. You can create the database using a database management tool or a command-line interface for the specific database system you are using (e.g., MySQL, PostgreSQL).
    
  - Copy the sample settings file for local development:

     ```
     cp drupal-basicsite-project/sites/example.settings.local.php drupal-basicsite-project/sites/default/settings.local.php
     ```

   - Open `drupal-basicsite-project/sites/default/settings.local.php` and add at the end the database connection settings. Here's an example of how it might look:
     
     ```
      $databases['default']['default'] = array(
        'database' => 'your_database_name',
        'username' => 'your_database_username',
        'password' => 'your_database_password',
        'prefix' => '',
        'host' => 'localhost',
        'port' => '3306',
        'namespace' => 'Drupal\\Core\\Database\\Driver\\mysql',
        'driver' => 'mysql',
      );
     ```

### 5. Start the Development Server:

   Launch the Symfony development server:

   ```
   symfony server:start -d
   ```

   Make sure you are in the root directory of your project when running this command. <br>
   Access your Drupal site at http://127.0.0.1:8000 in your browser.

## Managing Modules and Packages

Use Composer to manage Drupal modules and packages:

- **Install a Module:**

  ```
  composer require drupal/module-name
  ```

- **Remove a Module:**

  ```
  composer remove drupal/module-name
  ```

## Finding Modules

Explore and find Drupal modules on the official [Drupal Modules](https://www.drupal.org/project/project_module) website. Look for the Composer command under "Install with Composer" on a module's page.

## Contributing

Contributions are welcome! To report issues or contribute enhancements, open pull requests or create issues in the repository.

## License

This template is open-source and distributed under the [MIT License](LICENSE).

---

🚀 Happy coding and enjoy building your Drupal 10 project with Composer and Symfony integration! For any questions, feel free to reach out.
