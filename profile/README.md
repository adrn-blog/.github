## Hi there 👋

This organization is where the infrastructure to write and build blog posts for [adrian.pw](https://adrian.pw) lives.

This is based on [@dfm](https://github.com/dfm-io)'s blog and build machinery, so see there for context and more information!

- Each post lives in a repository within this organization with a name prefixed with `post--`. Take a look at [adrn-blog/template](https://github.com/adrn-blog/template) for more info about how new posts are created.
- The Jupyter notebook with each post's content gets executed within that repo's GitHub Actions environment and the executed version is pushed to the `executed` branch.
- Then, when the build workflow within the `adrn-blog/adrian.pw` repository is triggered (usually via a workflow dispatch), it finds all the `adrn-blog/post--*` repos and collects them as blog posts.
