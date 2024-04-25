The goal of the GitHub organization "Reproducible Reporting" is to facilitate
good practices for scientific publication and the research behind it.
By good practices, we mean at least the following:

- Make it easier to reproduce and reuse research.
- Increase the transparency of the writing process.
- Automate otherwise error-prone processes.

This is facilitated by collecting the source material and the data in one Git repository per publication.
The organization within each repository is streamlined as follows:

1. The [templates](https://github.com/reproducible-reporting/templates) repository
   is a [cookiecutter](https://github.com/cookiecutter/cookiecutter)
   template, providing an initial configurable setup for a new publication repository.
1. The Python packages
   [StepUp Core](https://github.com/reproducible-reporting/stepup-core) and
   [StepUp RepRep](https://github.com/reproducible-reporting/stepup-reprep)
   compile the publication source material into the final form for publication,
   presentation or journal submission.
   Their role is not limited to compiling LaTex sources.
   They also run post-processing scripts (e.g. using numpy, matplotlib), merge figures,
   archive datasets and keep track of dependencies between all these steps.
   StepUp makes it easy to tailor these workflows to the specific needs of any project.

Check out the [documentation](https://reproducible-reporting.github.io/stepup-reprep/) if you want to get started.
