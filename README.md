# Homebrew Tools

This repository is a personal [Homebrew](http://brew.sh) tap for a set of
[external commands][ext] useful for contributing.

[ext]: https://github.com/Homebrew/homebrew/blob/master/share/doc/homebrew/External-Commands.md#external-commands

This is a work in constant progress. I wrote these scripts to automate some of the work
I used to do manually when upgrading formulae and submitting pull requests to
the Homebrew repo.

Note: this intended as a *personal* tools set, expect things to be broken and
documentation to be outdated.

For a more general toolset, see [homebrew/dev-tools](https://github.com/Homebrew/homebrew-dev-tools).

## Usage

* `brew prepare <formula>`: prints some info about a formula, open its homepage
  in your browser, and open its source file for editing
* `brew done <formula> <change>`: use it when you’ve modified a formula. It’ll
  checkout a new branch, let you write a commit message, push to your GitHub
  fork and open the pull request page in your browser. `<change>` should be a
  single word describing the change (e.g. `1.0.3`, `head`, `test`, etc).
* `brew checkupdates [<formula> ...]`: check for formulae updates. It only
  supports GitHub and GNU FTP -hosted formulae for now.

All tools assume your local repo is up to date (i.e. you run `brew
update` regularly). I’m not responsible if you break your installation when
running one of these tools.

## Installation

Tap this repository:

    brew tap bfontaine/tools

### Dependencies

* `brew-checkupdates` requires `nokogiri`: `gem install nokogiri`
