# How to Contribute to Reproducible Reporting

Contributions are always welcome!
:thumbsup: :tada: :heart_eyes: :100:
These may also include minor corrections, clarifications, improved instructions, and so on.

New contributions are accepted in the form of a *pull request* (PR) from a *fork*.
If you are unfamiliar with this terminology, see GitHub's documentation on
[pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)
and [forks](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks).

Your pull request will be reviewed before it is merged.
During the review process, we may ask for changes or push additional commits.

If you think something should be improved but are not sure how,
it may be more appropriate to open an *issue* instead.
After some discussion in the issue, things may become clearer and you can still open a pull request.


## Automatic Cleanups with `pre-commit`

We use [pre-commit](https://pre-commit.com) on all repositories to automatically fix minor formatting issues.
To set up `pre-commit` locally, run the following:

- Install the pre-commit software (also available on conda or mamba).
  This is only needed once.
  ```bash
  pip install pre-commit
  ```
- Run this command in the directory of a Git repository.
  It assumes there is a `.pre-commit-config.yaml` file.
  ```bash
  pre-commit install
  ```
  This needs to be repeated for every Git repository you create or clone.

Once `pre-commit` is installed, it will automatically correct formatting when you run `git commit ...`.
When `pre-commit` makes corrections, it will abort the commit,
allowing you to check the result, add the modified files, and try a new commit.
You can also fix files before making a commit with the command: `pre-commit run --all`.


## Other Formatting Conventions

Not all formatting problems can be fixed automatically.
Try to keep the following in mind when editing Markdown and LaTeX files:

- We use `.editorconfig` to share the same configuration across different text editors we use.
  Make sure that your editor supports this file.
  See [https://editorconfig.org/](https://editorconfig.org/).
- Many errors can be avoided by using a live preview of your Markdown file as you write,
  and there are several ways to get such a live preview:

    - Many integrated development environments have this feature.
    - [StackEdit](https://stackedit.io/) is a convenient online Markdown editor with live preview.
    - Documentation written with MkDocs can be live previewed in a browser using `mkdocs serve`.
    - If you're using a basic editor, the following command can be used
      to generate a live preview every time you save the Markdown file:
      ```bash
      inotifywait . -m --include '.*\.md$' -e close_write | while read path event file; do echo rendering $file; pandoc $file -f gfm -o tmp.pdf --pdf-engine=weasyprint; xdg-open tmp.pdf; done
      ```
- Use [Semantic Line Breaks](https://sembr.org/) because it facilitates reviewing documentation changes.

For more details, check out the developer notes of specific projects:

- [StepUp Core Developer notes](https://reproducible-reporting.github.io/stepup-core/development/)
- [StepUp RepRep Developer notes](https://reproducible-reporting.github.io/stepup-reprep/development/)
