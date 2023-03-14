![REP REP](logo.png)

# About Reproducible Reporting

The goal of the GitHub organization "Reproducible Reporting" is to facilitate
good practices for scientific publication and the research behind it.
By good practices, we mean at least the following:

- Make it easier to reproduce and reuse research.
- Increase the transparency of the writing process.
- Automate otherwise error-prone processes.

This is facilitated by collecting the source material and the data in one Git repository per publication.
The organization within each repository is streamlined with two tools:

1. The [templates](https://github.com/reproducible-reporting/templates) repository
   is a [cookiecutter](https://github.com/cookiecutter/cookiecutter)
   template, providing an initial configurable setup for a new publication repository.
1. The Python package [RepRepBuild](https://github.com/reproducible-reporting/reprepbuild),
   compiles the source material, organized as in the template,
   into the final form for publication, presentation or journal submission.
   It does not only compile LaTex sources.
   In addition, it runs post-processing scripts (e.g. matplotlib),
   archives datasets and keeps track of dependencies between all these steps.
   Technicalities that would otherwise discourage good practices
   are automated (and imposed) by RepRepBuild.

# Future plans

- We will learn a lot from our initial attempts to get this
  up and running, so don't expect any API stability at this stage.
- More items in the [templates](https://github.com/reproducible-reporting/templates) repository:
  `latex-presentation`, `latex-phd-thesis`, `latex-msc-thesis`,
  `latex-note`, ...

# How to contribute

We have an organization-wide contributor guideline:
https://github.com/reproducible-reporting/.github/blob/main/CONTRIBUTING.md
