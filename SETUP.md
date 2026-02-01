# Local Development Setup Guide (macOS)

This guide will help you set up your local environment to run this website. Since macOS system Ruby is often outdated (v2.6), we need to install a modern version using Homebrew.

## Prerequisites

### 1. Install Xcode Command Line Tools
Required for compiling Ruby gems. Open Terminal and run:
```bash
xcode-select --install
```
Follow the pop-up prompt to install.

### 2. Install Homebrew
If you haven't installed Homebrew yet (check with `brew --version`), install it by running:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 3. Install Ruby
Install a modern version of Ruby (e.g., 3.3 or latest):
```bash
brew install ruby
```
After installation, you likely need to add the brew ruby path to your shell configuration (.zshrc). Run the command brew suggests, usually looking like:
```bash
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```
Verify installation:
```bash
ruby -v
# Should show ruby 3.x.x
```

## Running the Website

### 1. Install Jekyll and Bundler
```bash
gem install jekyll bundler
```

### 2. Install Dependencies
Run this in the project root directory:
```bash
bundle install
```

### 3. Start the Server
```bash
bundle exec jekyll serve
```

Your website will be available at `http://localhost:4000`.
