# ruby.org.au

The `ruby.org.au` site is a static site hosted with Github Pages.

* Content is in `/pages` as ERB templates
* Styles are `/stylesheets`, compiled using compass

## Build instructions

Building and deploying the site is done via rake tasks:

* `rake build:all` (aliased as default) compiles the site into `/site`
* `rake deploy` copies the _committed_ versions of all files in `/site` to the
  root of the `gh-pages` branch

So, your normal process would look something like this:

```
# ... Edit some content in /pages
git add pages/the-awesome-page.html.erb
rake build:all
git add site
git commit -m "Add an awesome page"
rake deploy
git push origin
# BOOM!
```
