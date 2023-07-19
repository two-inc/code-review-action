# code-review-action

Example Usage:

    name: Code Review (ChatGPT)

    on:
      pull_request:
        types:
          - opened
          - synchronize

    jobs:
      code-review:
        runs-on: self-hosted
        timeout-minutes: 20

        steps:
          - name: Code Review Action
            uses: two-inc/code-review-action@main
            with:
              github-token: "${{ secrets.GITHUB_TOKEN }}"
              openai-api-key: "${{ secrets.OPENAI_API_KEY }}"
