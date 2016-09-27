## Setting up Development

Before you add your bio, you probably want to get the code, right? To do this, we are going to fork the repo, clone it to our local machines, make edits, and push to master. Since this is not a formal code repo (e.g., we don't really need pull requests or continuous integration to test code) we are going to stick to working on the main branch (called master) and you are responsible for testing your changes locally, and then telling someone (@vsoch is a good person) if you mess up. If this freaks you out, you can also send your photo and bio to @vsoch and she will be glad to add it for you!

### Fork the repo
To contribute to the web based documentation, you should obtain a GitHub account and fork the <a href="https://github.com/radinformatics/radinformatics.github.io" target="_blank">Langlotz Lab Site</a> repository. Once forked, you will want to clone the fork of the repo to your computer. Let's say my Github username is vsoch, and I am using ssh:

```bash
git clone git@github.com:vsoch/radinformatics.github.io.git
cd radinformatics.github.io/
```

### Install a local Jekyll server
This step is required if you want to render your work locally before committing your changes. For the purpose of simplicity, we will articulate how to install Jekyll and its dependencies on a Mac.

```bash
brew install ruby
gem install jekyll
gem install bundler
bundle install
```

Now you can see the site locally by running the server with jekyll:

```bash
bundle exec jekyll serve
```

(Note: I don't use a Mac and I didn't install the packages using the Gemfile as above - so if you hit any errors with this process please submit an issue! If there are problems then @vsoch can make a dockerized development environment). 

This will make the site viewable at `http://localhost:4000/` If you want a nice look into how this works, you will probably want to look into the <a href="https://github.com/radinformatics/radinformatics.github.io/blob/master/_config.yml" target="_blank">config</a> file, or ask @vsoch (v) questions on Slack or the Google Group.


## Contributing a News Item

Each news item that is rendered automatically in the <a href="http://localhost:4000/feed" target="_blank">site feed</a> is done very simply - you just add a new markdown file to the folder `_posts/`. There are a few rules you must follow:

### Naming Convention
The name of the markdown file must be in the format `YYYY-MM-DD-meaningful-name.md` For example, `2016-09-23-first-post.md`

### Front End Matter
Jekyll has this thing they call <a href="https://jekyllrb.com/docs/frontmatter/" target="_blank">front matter</a> which is basically a header in your markdown file. For our news feed, the header should look something like this:

      ---
      title: "IIBIS Retreat at Stanford"
      author_profile: false
      categories: news
      sidebar:
        nav: "docs"
      ---
      
The title is self explanatory, as is the "categories" and "sidebar" (which you should not change). Actually, the only thing you need to change is the title.

Once the header is done, you simply write your post after it in <a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank">Markdown Syntax</a>. All and any HTML tags are fair game as well! Once you add the post, if you have set the category correctly to "news" it should show up in the site feed. It's that easy!


## Contributing to a Page

All of the pages are in the <a href="https://github.com/radinformatics/radinformatics.github.io/blob/master/pages" target="_blank">pages</a> folder, named in a somewhat logical manner. If you want to edit content for a page, just edit the corresponding file. If you need to do something more advanced like edit a sidebar, you should look at the <a href="https://github.com/radinformatics/radinformatics.github.io/blob/master/_data/navigation.yml" target="_blank">navigation data</a> yml document, which renders into the navigation.

## Adding your bio

Full instructions for adding your bio are included in [adding-your-bio.md](adding-your-bio.md)

Now that you are ready to go, you might want to look at [working-with-github.md](working-with-github.md)


