# Logeman Lab website

A minimal Jekyll website for the Logeman Lab. It uses plain HTML and CSS, with
no theme, JavaScript, external framework, or Jekyll plugin.

## Install dependencies

Jekyll requires Ruby 2.7 or newer. Check the active Ruby first:

```sh
ruby --version
```

macOS includes an older system Ruby, so install a current Ruby with Homebrew if
the version reported above is lower than 2.7:

```sh
brew install ruby
echo 'export PATH="$(brew --prefix ruby)/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

Install Bundler, move into this project, and install the gems listed in the
`Gemfile`:

```sh
gem install bundler
cd /Users/brandonlogeman/Desktop/lab_website
bundle config set --local path vendor/bundle
bundle install
```

The local bundle path keeps project gems out of the system Ruby directories.
Bundler will also create `Gemfile.lock` the first time dependencies are
installed.

## Run locally

```sh
cd /Users/brandonlogeman/Desktop/lab_website
bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000> in a browser. Jekyll watches the project files
and rebuilds the site when they change. Stop the server with `Ctrl+C`.

## Build without starting a server

```sh
bundle exec jekyll build
```

The generated site will be written to `_site/`, which is ignored by Git.
