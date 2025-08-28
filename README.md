# Drupal Onboarding Project

Practice repository using **Drupal 10** and **Lando**.  
This repo includes basic site building tasks: URL alias patterns, a Projects listing page, and a “Latest Projects” sidebar block — all stored in configuration and versioned in Git.

---

## Requirements

- Docker + [Lando](https://lando.dev/) installed
- [Composer](https://getcomposer.org/) 2.x
- Git

> **Note:** The local domain `drupalonboarding.lndo.site` is created by Lando and only works on your machine.

---

## Quick Start (first-time setup)

```bash
# Clone the repository
git clone https://github.com/VictoriaCamFo/drupal-onboarding.git
cd drupal-onboarding

# Start containers (PHP, DB, etc.)
lando start

# Install PHP dependencies (creates /vendor)
lando composer install

# Install the site from exported configuration (uses config/sync)
# This creates the DB and imports all configuration automatically.
lando drush si --existing-config -y

# Clear caches and get a one-time admin login link
lando drush cr
lando drush uli

