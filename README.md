# kitty - [AngularJS](http://angularjs.org/) based DSL for mathematics. 

***

[![Build Status](https://secure.travis-ci.org/angular-ui/bootstrap.png)](http://travis-ci.org/angular-ui/bootstrap)

## Brief Description

* Warning: Kitty is not yet stable enough to be useful. *

We hope that kitty will grow into a useful set of angular modules that make writing HTML5/JS interactive resources for mathematics education easier. It inherits its build tools from [angular-ui/bootstrap](http://angular-ui.github.com/bootstrap/) and is designed to work alongside that framework. It's a separate project because kitty has a domain specific aim. It's only going to be useful if you are a mathematics educator and we've already built something you need. 

Contributions to kitty will be welcome once we are stable enough to accept them, and will follow the pattern established by angularJS and angular-ui/bootstrap.

Remaining notes are inherited from angular-ui/bootstrap and mostly apply

### Customizability

All the directives in this repository should have their markup externalized as templates (loaded via `templateUrl`). 

### Take what you need and not more

Each directive has its own AngularJS module without any dependencies on other modules or third-pary JavaScript code. In practice it means that you can **just grab the code for the directives you need** and you are not obliged to drag the whole repository.

### Quality and stability

Directives should work. All the time and in all browsers. This is why all the directives have a comprehensive suite of unit tests. All the automated tests are executed on each checkin in several browsers: Chrome, ChromeCanary, Firefox, Opera, Safari, IE9.
In fact we are fortunate enough to **benefit from the same testing infrastructure as AngularJS**!

## Contributing to the project - * when we get are ready, but please not yet! *

We are always looking for the quality contributions! Please check the [CONTRIBUTING.md](CONTRIBUTING.md) for the contribution guidelines.

### Development
#### Prepare your environment
* Install [Node.js](http://nodejs.org/) and NPM (should come with)
* Install global dev dependencies: `npm install -g grunt testacular`
* Instal local dev dependencies: `npm install` while current directory is bootstrap repo

#### Run unit tests
* Start testacular server: `grunt server`
* Run test: `grunt test-run`

#### Before commit
* Build the whole project: `grunt` - this will run `lint`, `test`, and `concat` targets

### Release
* Bump up version number in `package.json`
* Commit the version change with the following message: `chore(release): [version number]`
* tag
* push changes and a tag (`git push --tags`)
* switch to the `gh-pages` branch: `git checkout gh-pages`
* copy content of the dist folder to the main folder
* Commit the version change with the following message: `chore(release): [version number]`
* push changes
* switch back to the `main branch` and modify `package.json` to bump up version for the next iteration
* commit (`chore(release): starting [versio number]`) and push

Well done! (If you don't like repeating yourself open a PR with a grunt task taking care of the above!)
