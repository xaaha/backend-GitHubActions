# backend-GitHubActions

- Testing `Trigger and Wait`

- Artifact

```shell
# name: Get and Store Pr Number
# on:
#   repository_dispatch:
#     types: [pr-input]

# jobs:
#   print_pull_request_number:
#     runs-on: ubuntu-latest
#     steps:
#       - name: Store Pull Request Number
#         run: |
#           echo "Base URL: www.example.com/pr-${{ github.event.client_payload.prNumber }}"
#           echo ${{ github.event.client_payload.prNumber }} > prNumber.txt
#       - name: Upload prNumber as artifact
#         uses: actions/upload-artifact@v2
#         with:
#           name: prNumber
#           path: prNumber.txt

# # it does not work since artifact can't be shared between different workflows.


```
