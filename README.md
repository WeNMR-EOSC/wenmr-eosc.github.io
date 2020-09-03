# WeNMR site based on the Jekyll template [Minimal Mistakes](http://mmistakes.github.io/minimal-mistakes)

For more information on the template and folder organization, visit the [original author's
web page](http://mmistakes.github.io/minimal-mistakes/theme-setup/).

## Getting Started

To ensure whatever you create/change appears as faithfully as possible after pushing to the main repository, install the version of Ruby and the gems used by Github. See a list [here](https://pages.github.com/versions/).

### Installation Instructions (updt. Feb. 2016)

1. Install Ruby

Make sure you have an active installation of the Ruby programming language:
```bash
$ ruby -v
rvm --default use ruby-2.6.3
```

2. Install Bundler
```bash
gem install bundler
```

3. Clone this repository and install all dependency Gems with Bundler

```bash
git clone https://github.com/WeNMR-EOSC/wenmr.github.io.git
cd wenmr.github.i
bundle install
```

4. Adapt the settings in _config.yml accordingly
In order for links to properly work, the `url` setting in must be set accordingly, otherwise you will be redirected to the live version. This sets all the `site.url` variable calls throughout _layouts/,  _includes/, etc.

```yaml
url: "" # Empty string will render the page successfully locally. Do not commit it to the main repository!
incremental: true # This will be disabled by Github, but is useful for testing changes locally!
```

### Running the website locally

To preview changes, which you should always do before committing anything or making any pull requests, run the web server locally using the following:

```bash
    $ bundle exec jekyll serve --watch
```

### Small utility to create a new post automatically. Quick and dirty replacement of `octopress new post`

```python
    $ python _utilities/create_new_article.py 'A Random Post'
```

4. For updating jeckyll and bundle

```bash
    $ gem update jekyll
    $ gem update bundle
