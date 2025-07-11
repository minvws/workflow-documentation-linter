# Documentation linter

- This pipeline is designed to run [DavidAnson Markdown linter](https://github.com/DavidAnson/markdownlint?tab=readme-ov-file#markdownlint)
when a pull request is created
- The pipeline is designed to be as generic as possible, so they can be easily reused in any project.
- This repository is a part of the generic GitHub Actions pipeline collection that can be used in any project.

## Usage

The documentation linter workflow is called from a workflow in the private repository.
Here is a basic example of how you can integrate it in your project.

<details>
  <summary>Example workflow</summary>

This workflow is executed automatically when a pull request is created or updated that includes changes to Markdown files (**.md).

```yml
name: Documentation linter

on:
    pull_request:
        paths:
            - '**.md'

jobs:
    documentation-linter:
    uses: minvws/workflow-documentation-linter/.github/workflows/repo-sync.yml@main
```

</details>

## Contributing

If you want to contribute a new pipeline, please check the reusable workflow guidelines in the
[GitHub documentation](https://docs.github.com/en/actions/using-workflows/reusing-workflows#creating-a-reusable-workflow).
