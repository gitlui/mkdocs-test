# mkdocs-test

This is a test project to test the capabilities of [MkDocs](https://www.mkdocs.org/) and [material for MkDocs](https://squidfunk.github.io/mkdocs-material/) using GitHub-Pages which are hosted here:

https://gitlui.github.io/mkdocs-test/

# The workflow
1. Change the markdown in the repository
2. Commit the code to main/master
3. The github action detects the change and builds and publishes a new version using MkDocs commands
4. The pages are commited automatically to the branch gh-pages
5. The branch gh-pages is configured in GutHub Pages as source
6. The new page version is published