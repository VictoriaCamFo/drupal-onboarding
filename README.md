# Drupal Onboarding Project

This is the practice repository using **Drupal 10** and **Lando**.

## 🚀 Requirements
- [Lando](https://docs.lando.dev/getting-started/installation.html) installed on your machine.
- [Composer](https://getcomposer.org/) (optional, if you want to manage dependencies directly).

## 📦 Installation

# Clone the repository
git clone https://github.com/VictoriaCamFo/drupal-onboarding.git
cd drupal-onboarding

# Start the local environment (Docker via Lando)
lando start

# Install PHP dependencies (creates the /vendor directory)
lando composer install

# First-time site install from exported configuration (uses config/sync)
# This will create the DB and import all configuration automatically
lando drush si --existing-config -y

# For already-installed sites, apply config changes instead of site install:
# lando drush cim -y

# Clear caches and get a one-time login link to the admin
lando drush cr
lando drush uli
http://drupalonboarding.lndo.site/
