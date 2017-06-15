# Drupal 8 Headless Local => Deployment Workflow

## Requirements
- [Docker4Drupal] (docker4drupal.org). Please follow documentation for usage. There will be a section below to summary some main points.
- [Composer Template for Drupal Projects] (https://github.com/drupal-composer/drupal-project)

## Workflow

Please refer to `docker-sync.yml` and `docker-compose.yml` as example.

### Start Project
This project is based on the single site setup. Please refer to Docker4Drupal for multi site setup.

    - composer create-project drupal-composer/-drupal-project:8.x-dev some-dir --stability dev --no-interaction
    - docker-sync start
    - docker-compose up -d
Once this step is done, you can go to `http://drupal.docker.localhost:8000` to start setup and develop

**TODO**

- Run install command to skip install screen.

### Local
- Drupaling like you usually do!
- When you get to a stopping point, run `drush config-export -y` to generate configuration. Configuration will be exported to `config/sync` directory. If you are using Docker4Drupal, make sure you wrap `drush` command with `docker-compose` command.
- Commit and push your site configuration.

### Deployment
**TODO**

### Docker4Drupal
**TODO**