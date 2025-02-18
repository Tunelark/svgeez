# Contributing to svgeez

There are a couple ways you can help improve svgeez:

1. Fix an existing [issue][issues] and submit a [pull request][pulls].
1. Review open [pull requests][pulls].
1. Report a new [issue][issues]. _Only do this after you've made sure the behavior or problem you're observing isn't already documented in an open issue._

## Getting Started

svgeez is developed using Ruby 2.4.10 and is additionally tested against Ruby 2.5, 2.6, and 2.7 using [CircleCI](https://app.circleci.com/pipelines/github/jgarber623/svgeez).

Before making changes to svgeez, you'll want to install Ruby 2.4.10. It's recommended that you use a Ruby version managment tool like [rbenv](https://github.com/rbenv/rbenv), [chruby](https://github.com/postmodern/chruby), or [rvm](https://github.com/rvm/rvm). Once you've installed Ruby 2.4.10 using your method of choice, install the project's gems by running:

```sh
bundle install
```

…from the root of the project.

In order for the test suite to run properly, [SVGO](https://github.com/svg/svgo) must be installed (and the `svgo` command must be available in your `PATH`). This is most easily achieved by installing [Node.js](https://nodejs.org) and running:

```sh
npm install -g svgo
```

## Making Changes

1. Fork and clone the project's repo.
1. Install development dependencies as outlined above.
1. Create a feature branch for the code changes you're looking to make: `git checkout -b my-new-feature`.
1. _Write some code!_
1. Build (`bin/rake build`) and install (`bin/rake install`) your updated code.
1. If your changes would benefit from testing, add the necessary tests and verify everything passes by running `bin/rake`.
1. Commit your changes: `git commit -am 'Add some new feature or fix some issue'`. _(See [this excellent article](https://chris.beams.io/posts/git-commit/) for tips on writing useful Git commit messages.)_
1. Push the branch to your fork: `git push -u origin my-new-feature`.
1. Create a new [pull request][pulls] and we'll review your changes.

## Code Style

Code formatting conventions are defined in the `.editorconfig` file which uses the [EditorConfig](http://editorconfig.org) syntax. There are [plugins for a variety of editors](http://editorconfig.org/#download) that utilize the settings in the `.editorconfig` file. We recommended you install the EditorConfig plugin for your editor of choice.

Additionally, [Rubocop](https://github.com/bbatsov/rubocop) can be used to help identify possible trouble areas in your code. Run `bin/rubocop` to generate Rubocop's static code analysis report.

Your bug fix or feature addition won't be rejected if it runs afoul of any (or all) of these guidelines, but following the guidelines will definitely make everyone's lives a little easier.

[issues]: https://github.com/jgarber623/svgeez/issues
[pulls]: https://github.com/jgarber623/svgeez/pulls
