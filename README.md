# Drupal Onboarding Project

This is the practice repository using **Drupal 10** and **Lando**.

## 🚀 Requirements
- [Lando](https://docs.lando.dev/getting-started/installation.html) installed on your machine.
- [Composer](https://getcomposer.org/) (optional, if you want to manage dependencies directly).

## 📦 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/DrupalOnboarding.git
   cd DrupalOnboarding
   
   lando start
   lando drush cim -y
   lando drush cr
http://drupalonboarding.lndo.site/
