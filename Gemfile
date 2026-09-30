source "https://rubygems.org"
# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
# The site is built by .github/workflows/jekyll-gh-pages.yml, not by the
# GitHub Pages builder, so the github-pages gem is not needed. It pins
# jekyll-remote-theme 0.4.3, which caps rubyzip below 3.0.
gem "jekyll", "~> 3.10"
gem "kramdown-parser-gfm", "~> 1.1"
gem "webrick", "~> 1.8"
# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "rake"
  gem "jekyll-seo-tag"
  gem "jekyll-include-cache"
  gem "just-the-docs"
  # Formerly supplied by github-pages. The first three render
  # MAINTAINERS.md, which has no front matter, as a themed page titled by
  # its heading; the last rewrites relative .md links to the built pages.
  gem "jekyll-optional-front-matter"
  gem "jekyll-titles-from-headings"
  gem "jekyll-default-layout"
  gem "jekyll-relative-links"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
