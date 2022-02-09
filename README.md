# Setup Guidelines

1. Install [Ruby](https://rubyinstaller.org/downloads/) using the ruby installer:
    > Use the latest version X64

2. Install [Jekyll](https://jekyllrb.com/) using the following command:
    > `gem install jekyll bundler`

    Read more about Jekyll in the [official documentation](https://jekyllrb.com/docs/)....

3. Install bundle for the project using the following command:
    > `bundle install`

4. Build the site and serve it locally at [`http://localhost:4000`](http://localhost:4000) using the following command:
    > `bundle exec jekyll serve`


    > #### Note:
    > Pass the `--livereload` option to serve to automatically refresh the page with each change you make to the source files:
    `bundle exec jekyll serve --livereload`

5. Deploying the cms
Run `git remote add heroku https://git.heroku.com/content-cms.git` to add heroku repo to local git.
Then run `git push heroku develop:master` to deploy to heroku
The app can then be accessed at https://content-cms.herokuapp.com/