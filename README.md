# byu-cs.github.io
Class Descriptions for BYU CS department classes
Other stuff to come in the future

## Jekyll

This site is built using Jekyll, allowing for easily writing most of the content in markdown, which is then transformed into HTML with Jekyll and hosted via GitHub. The site theme is a modified form of [@jasonlong][2]'s [Cayman theme][4] on [GitHub Pages][3]. However, this should be easy to change in the future if someone finds something better out there, or wants to make their own.

## Development

For development, the best work flow would be to fork this repo (if you are not a member of the BYU-CS org), develop locally, make commits to your forked repo, and then submit a pull request with your finished changes. Running Jekyll locally will allow you to see your changes live on your local machine before pushing them to GitHub.

### Installing Jekyll

Jekyll is supported on OS X and Linux. It is not officially supported on Windows, but there are supposedly ways to get it running. For anyone running another OS, you're on your own.

The gist of it all is the following steps:

1. Install Ruby (which will include the gem package manager for Ruby)
2. Install Bundler: `$ gem install bundler`
3. Fork & clone this repo
4. Enter the repo directory and install dependencies: `$ bundle install`

At this point, all the dependencies should be resolved and installed, and you should be good to run it on your machine.

### Running Jekyll locally

To run it locally, make some changes and use the following command: `$ jekyll serve`

Alternatively, you can keep Jekyll running and it should detect changes and update the affected pages automatically. Remember to force reloading the page and sometimes clean out the generated files with `$ jekyll clean` if needed.


### Organization

This section describes the general organization of the repository. Jekyll takes files that have YAML front matter (the section that is prefixed and suffixed with `---` on some pages) and transforms them accordingly. The attributed `layout` determines which layout from the root folder `_layouts` to use. The folder `_includes` contains chunks of HTML that are reused and inserted into pages or layouts. The folder `_site` contains the built product from Jekyll and is ignored in the Git repo. 

#### Courses

The folder `_courses` contains all of the individual course pages. It is configured as a collection within Jekyll, meaning that Jekyll will collect all of the pages within that have YAML front matter, transform them to HTML, and then make them available anywhere in the system. On the `courses/index.html` page, we then call and populate the page with the listing of all of the courses. This allows for ease of adding a course, just copy the provided template on `courses/howto.md`, add it as a markdown file in the `_courses` directory, and Jekyll will add it where it needs to be.

#### Adding pages

To add standalone pages, you should be able to look at the repo and get the general sense of how to go about adding things. Any root level folder should contain an `index.html` file, like the root directory for the repo or `./courses`, for example. Past that, you can add standalone HTML pages that do not contain any YAML front matter (Jekyll doesn't touch anything that doesn't have front matter), add HTML pages with front matter (like `index.html` in the root directory), or markdown pages with front matter (like `courses/howto.md`). The latter two will be transformed by Jekyll and will reside at `index.html` and `courses/howto.html` respectively.

#### Configuration

Some important configuration can be done in the file `_config.yml`. Please, check the Setup section in that file.

##### baseurl

`baseurl` parameter is required in the case the site doesn't sit on the root of the domain. For example: http://pietromenna.github.io/jekyll-cayman-theme

In the case above the `baseurl` should be set to "/jekyll-cayman-theme".

In the case the site sits in the root, you can leave `baseurl` as empty "".

## Conclusions

Hopefully, this site will enable easy gathering and dissemination of information among BYU CS students for other students. Feel free to ask questions here, or on the [BYU CS Slack](https://byucompsci.slack.com).

## Theme License

The Cayman theme is licensed under a [Creative Commons Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/) license.

[1]: http://jekyllrb.com/
[2]: https://github.com/jasonlong
[3]: http://pages.github.com/
[4]: https://github.com/jasonlong/cayman-theme