# How to Preview Locally

## Option 1: Using Conda Environment (For the `apple` environment)

1. Activate your conda environment and set up Ruby:
   ```bash
   conda activate apple
   conda install -c conda-forge ruby=3.2 -y
   conda install -c conda-forge compilers make -y
   export PATH="/Users/daniil/miniconda3/envs/apple/bin:$PATH"
   ```

2. Install bundler:
   ```bash
   gem install bundler
   ```

3. Install dependencies:
   ```bash
   bundle install
   ```

4. Start the local server:
   ```bash
   export PATH="/Users/daniil/miniconda3/envs/apple/bin:$PATH"
   bundle exec jekyll serve
   ```

5. Open your browser to: `http://localhost:4000`

**Note:** Make sure to export the PATH to use the conda Ruby before running bundle commands.

## Option 2: Using rbenv (Alternative)

1. Install rbenv and Ruby:
   ```bash
   brew install rbenv ruby-build
   rbenv init
   rbenv install 3.2.0  # or latest 3.x version
   rbenv local 3.2.0
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Start the local server:
   ```bash
   bundle exec jekyll serve
   ```

4. Open your browser to: `http://localhost:4000`

## Option 2: Using Homebrew Ruby

1. Install Ruby via Homebrew:
   ```bash
   brew install ruby
   ```

2. Update your PATH (add to ~/.zshrc or ~/.bash_profile):
   ```bash
   export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
   ```

3. Install bundler:
   ```bash
   gem install bundler
   ```

4. Install dependencies:
   ```bash
   bundle install
   ```

5. Start the local server:
   ```bash
   bundle exec jekyll serve
   ```

6. Open your browser to: `http://localhost:4000`

## Option 3: Using GitHub Pages (No Local Preview)

You can push your changes to GitHub and GitHub Pages will build and serve your site automatically. No local setup needed!

1. Commit and push your changes:
   ```bash
   git add .
   git commit -m "Update site"
   git push
   ```

2. Your site will be available at: `https://daniilmelnichenko.github.io`

## Option 4: Using Docker (if you have Docker installed)

1. Build and run with Docker:
   ```bash
   docker-compose up
   ```

2. Open your browser to: `http://localhost:4000`

## Troubleshooting

- **Port already in use**: Use `bundle exec jekyll serve --port 4001` to use a different port
- **Dependencies issues**: Try `bundle update` to update gem versions
- **Permissions error**: You may need to use `sudo` (not recommended) or install gems to user directory
