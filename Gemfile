# frozen_string_literal: true

source "https://rubygems.org"

git_source(:github) {|repo_name| "https://github.com/#{repo_name}" }

# gem "jekyll", "~ 3.9.0"

# This is the default theme for new Jekyll sites. You may change this to anything you like.
# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
  gem "minima", "~> 2.5.1"
  gem "kramdown", ">= 2.3.0"
  gem "rake"
end

group :test do
  gem 'html-proofer'
end
