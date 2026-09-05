source "https://rubygems.org"

# The github-pages gem pins the same versions GitHub Pages builds with, so a
# local `bundle exec jekyll serve` matches what actions/jekyll-build-pages@v1
# produces in CI. It already bundles jekyll-seo-tag and jekyll-sitemap -- the
# two plugins listed in _config.yml -- so they are not repeated here.
gem "github-pages", group: :jekyll_plugins

# No longer part of the standard library on Ruby 3.0+; jekyll serve needs it.
gem "webrick", "~> 1.8"
