# How to contribute to Reproducible Reporting

Contributions are always welcome!
:thumbsup: :tada: :heart_eyes: :100:
These may also include minor corrections, clarifications, improved instructions, etc.

New contributions are accepted in the form of a *pull request* (PR), which is reviewed before merging.
During the review process, we may ask for changes or push additional commits.
If you think something should be improved, but you are not sure how,
it may be more appropriate to open an *issue* instead.
After some discussion in the issue, things may become clearer and you can still open a pull request.

We use [pre-commit](https://pre-commit.com) on all repositories.
To set up `pre-commit` locally, run the following:

- Install the pre-commit software (also avialable on conda or mamba).
  This is only needed once.
  ```bash
  pip install pre-commit
  ```
- The following needs to be run in the directory of a git repository.
  It assumes that a `.pre-commit-config.yaml` file exists.
  ```bash
  pre-commit install
  ```
  This must be repeated for every Git repository created or cloned.

Once `pre-commit` is installed, it will automatically correct formatting when you run `git commit ...`.
When `pre-commit` makes corrections, it aborts the commit,
allowing you to check the result, add the modified files and try a new commit.
You can also fix files before committing with the command: `pre-commit run --all`.

Not all formatting problems can be fixed automatically.
Try to keep the following in mind when editing.

- We use `.editorconfig` to share the same configuration across different text editors we use.
  Make sure your editor supports this file.
  See https://editorconfig.org/
- Many errors can be avoided by using a live preview of your Markdown file as you write.
  Many integrated development environments have this feature.
  If you're using a more basic editor, the following command can be used
  to generate a live preview everytime you save the markdown file:
  ```bash
  inotifywait . -m --include '.*\.md$' -e close_write | while read path event file; do echo rendering $file; pandoc $file -f gfm -o tmp.pdf --pdf-engine=weasyprint; xdg-open tmp.pdf; done
  ```

- Put each sentence on its own line.
  This makes reviewing changes a lot easier.
