Hermetic Operator PR Builds  - Implementation Plan
Jira: RHOAIENG-87557
Design Doc: Gated Artifacts-Promoter (GAP)

Summary:
Enable operator-processor
To trigger on PR events, limited to specific branches
Handle the PR event specific logic to add the comment on the PR to trigger the tekton build
Component images tags are formed based on the release branch name (rhoai-x.y)
We need to introduce a default image tag in case the PR build is running from the non-release branch
The default image tag can be same as latest rhoai-x.y (the same way we handle it for early-gate defaults)
Update tekton PR pipeline
To not trigger on each PR
Have proper output-image tags
Check the possibility of dynamic image tags containing PR numbers
