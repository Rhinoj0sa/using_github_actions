# Create Issue from PR

This GitHub Action workflow creates an issue from a pull request when it is opened or edited.

## Prerequisites

- GitHub repository
- GitHub Actions enabled
- GitHub CLI installed

## Installation

1. Clone the repository.
2. Ensure you have the necessary permissions to create workflows in the repository.

## Usage

1. Create a file named `.github/workflows/create_issue_from_pr.yaml` in your repository.
2. Add the following content to the file:

    ```yaml
    name: Create Issue from PR

    on:
      pull_request:
        types: [opened, edited]

    jobs:
      create-issue:
        runs-on: ubuntu-latest

        steps:
        - name: Extract PR data
          id: extract_data
          run: |
            PR_TITLE="${{ github.event.pull_request.title }}"
            PR_BODY="${{ github.event.pull_request.body }}"
            echo "PR_TITLE=$PR_TITLE" >> $GITHUB_ENV
            echo "PR_BODY=$PR_BODY" >> $GITHUB_ENV

        - name: Create Issue
          env:
            GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          run: |
            gh issue create --title "Issue from PR: $PR_TITLE" --body "$PR_BODY"
    ```

3. Commit and push the changes to your repository.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License.