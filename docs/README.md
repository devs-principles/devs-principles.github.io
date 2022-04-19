
## Building and start your site locally

```shell
$ bundle install 
$ bundle exec jekyll serve --drafts
Configuration file: ../docs/_config.yml
            Source: ../docs
       Destination: ../docs/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
       Jekyll Feed: Generating feed for posts
                    done in 0.213 seconds.
 Auto-regeneration: enabled for '../docs'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

To preview your site, in your web browser, navigate to http://localhost:4000.

## Update github-pages gem

Jekyll is an active open source project that is updated frequently. 
**Note:** 
If the github-pages gem on your computer is out of date with the github-pages gem on the GitHub Pages server, 
your site may look different when built locally than when published on GitHub.
To avoid this, regularly update the github-pages gem on your computer.

```shell
$ bundle update github-pages
Fetching gem metadata from https://rubygems.org/.........
Resolving dependencies....
...
Using github-pages 225
Bundler attempted to update github-pages but its version stayed the same
Bundle updated!
```

## References

- https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll

