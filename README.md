# AzureSignTool x86 Windows build system powered by GitHub Actions

## About
- `.github/workflows/build.yml` - Builds the FFmpeg git submodule every time a tag is added.
- `.github/workflows/update-azuresigntool.yml` - Checks for a new AzureSignTool release tag daily and updates the submodule and adds a new release tag, triggering the Build workflow.

## How to configure
1. Enable the GitHub Actions workflows
2. A personal GitHub user token is used for the workflows to trigger each other. You will need to create a personal access token in the GitHub Developer Settings menu with the `repo` permissions. Then, add this token in your repo's Secrets and variables Settings menu as a secret with the name `PUSH_TOKEN`.
