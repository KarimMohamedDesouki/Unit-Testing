# PHP Unit Testing for User Management and Factorial Calculation

This project provides unit tests for user management and factorial calculation functionalities using PHP. It ensures that the core functionalities of user operations (like creation, deletion, and retrieval) and the mathematical operation for calculating factorial are working correctly.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Introduction

This project aims to demonstrate how to write and run unit tests for common functionalities in PHP. The focus is on two main aspects:

1. **User Management**: Includes operations such as user creation, deletion, and retrieval.
2. **Factorial Calculation**: A simple mathematical function to calculate the factorial of a number.

## Installation

Follow these steps to set up the project:

```bash
# Clone the repository
git clone https://github.com/yourusername/php-unit-testing-user-factorial.git

# Navigate into the project directory
cd php-unit-testing-user-factorial

# Install dependencies
composer install
```

## Usage

```bash
vendor/bin/phpunit


require 'vendor/autoload.php';

use YourNamespace\UserManager;
use YourNamespace\MathUtils;

// User Management Example
$userManager = new UserManager();
$userManager->createUser('john_doe', 'password123');
$user = $userManager->getUser('john_doe');
echo $user->getUsername(); // Output: john_doe

// Factorial Calculation Example
echo MathUtils::factorial(5); // Output: 120
```

## Features


  * User Management
    * Create User
      
  * Factorial Calculation
    * Calculate factorial of a given number

## Dependencies
PHP >= 7.4
PHPUnit >= 9.0


## Configuration
No specific configuration is required for this project. Ensure you have the necessary dependencies installed via Composer.

## Documentation

User Management
The UserManager class handles user operations:

```bash
php
Copy code
class UserManager {
    public function createUser(string $username, string $password): bool;
    public function deleteUser(string $username): bool;
    public function getUser(string $username): ?User;
}
```
Factorial Calculation
The MathUtils class provides a method to calculate factorial:

```bash
php
Copy code
class MathUtils {
    public static function factorial(int $number): int;
}
```
## Examples

**User Management**

```bash
$userManager = new UserManager();
$userManager->createUser('john_doe', 'password123');
$user = $userManager->getUser('john_doe');
echo $user->getUsername(); // Output: john_doe
```

**Factorial Calculation**

```bash
echo MathUtils::factorial(5); // Output: 120
```


##  Troubleshooting
If you encounter any issues, ensure that all dependencies are correctly installed. Running composer install again may resolve some issues.


##   License
This project is licensed under the MIT License - see the LICENSE file for details.
Feel free to customize this README further to better match your project's specific details and requirements.
