# Heroku Angular sample

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.7.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

---

## TL;DR

```bash
# Create your application using `ng-cli`
ng new YOUR-HEROKU-DYNO-NAME

# Navigate to your application folder and create a Git repository
cd YOUR-HEROKU-DYNO-NAME/
git init

# Create a Heroku Dyno using Node.js buildpack
heroku apps:create YOUR-HEROKU-DYNO-NAME --buildpack https://github.com/heroku/heroku-buildpack-nodejs

# Add static buildpack as secondary
heroku buildpacks:add https://github.com/heroku/heroku-buildpack-static --index 2

# Create `static.json` with Heroku buildpack settings
# https://github.com/magnobiet/heroku-angular/blob/master/static.json

# Add `postinstall` script with build command to your `package.json`
# https://github.com/magnobiet/heroku-angular/blob/master/package.json#L15

# Commit all changes
git add .
git commit -m "Initial commit"

# Deploy your application
git push heroku master

# In your browser navigate to https://YOUR-HEROKU-DYNO-NAME.herokuapp.com/
```

### References

- https://github.com/angular/angular-cli
- https://github.com/heroku/heroku-buildpack-nodejs
- https://github.com/heroku/heroku-buildpack-static
