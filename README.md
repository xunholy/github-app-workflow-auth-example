# Github App Authentication in Github Workflow

This repo demonstrates how to impersonate a GitHub App when secrets.GITHUB_TOKEN's limitations are too restrictive and a personal access token is not suitable.

In this example we use [bubkoo/use-app-token@v1](https://github.com/bubkoo/use-app-token) Github Action.

It's strongly recommended to also use the [styfle/cancel-workflow-action@0.6.0](https://github.com/styfle/cancel-workflow-action) Github Action or similar to ensure that previous running workflows are cancelled. This is due to a concurrency issue where two commits can be pushed and the second commit will not dismiss the auto-approval of the first commit and could introduce breaking changes that are still approved.
