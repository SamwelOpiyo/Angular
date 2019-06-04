[![Build Status](https://travis-ci.org/SamwelOpiyo/Angular.svg?branch=master)](https://travis-ci.org/SamwelOpiyo/Angular)

# Beerbank

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.1.3.

## CI/CD Setup.

### Generating a Github Token.

A github token is needed in order access and clone the repository containing infrastructure and application configuration/provisionment scripts.

Open https://github.com/settings/tokens and generate a new token. Ensure you check the *REPO* check box so that the token can have permissions to pull from private repositories.

### Environment Variables Setup.

Open https://travis-ci.org/{user/organization}/{repository}/settings for example https://travis-ci.org/SamwelOpiyo/Angular/settings and set the following environment variables:

* DOCKER_HUB_PASSWORD
* DOCKER_HUB_USER
* GITHUB_TOKEN
* GCP_MAIN_SERVICE_ACCOUNT :To get this value you will need the path of admin service account generated to run terraform. Use `base64 {path_to_SA} | paste -sd ''` to obtain it. For example in our case navigate to configurations repository, terraform then run `base64 service_account_keys/main_service_account.json | paste -sd ''`.

### Activating Repository for CI/CD.

Open https://travis-ci.org/{user/organization}/{repository} for example https://travis-ci.org/SamwelOpiyo/Angular and click on *Activate repository*.

## Project setup.

### Development server.

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

### Code scaffolding.

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build.

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

### Running unit tests.

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests.

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

### Further help.

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
