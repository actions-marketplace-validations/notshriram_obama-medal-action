# obama-medal-action
Github Action that posts an obama meme when a person merges his own pull request


## Example Usage
Add this yml file into your .github/workflows directory:

```yaml
name: MergeComment

# Controls when the workflow will run
on:
  # Triggers the workflow on pull request event (closed event)
  pull_request:
    types:
      - closed

jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v2
      - name: Obama Medal Action
        # You may pin to the exact commit or the version like:
        # uses: notshriram/obama-medal-action@2d97e4b58a804147d1395357831a8e9cd5dc1759
        uses: notshriram/obama-medal-action@Alpha
        with:
          # GitHub token
          GITHUB_TOKEN: ${{secrets.GITHUB_TOKEN}}

```
