# Test release pr label version
> release prs with labels

The goal is to add labels to release pr's to indicate what type of release should be applied.  
This follows the [semver](https://semver.org/). IE Major.Minor.Patch.

Once the pr is merged to the release branch (in this case, `main`), release action will get the last merged pull request,  
and check if any release labels have been added.

## Actions explained
- labeler-validator: checks that the required labels are added.  
  This should be used with the branch protection rules so that a release pr cannot be merged if the correct label is not selected.
- release:
  The action that will build, and create the version for the release
- Wil add a `release:version-required` if no release label is added.
  - If a release label is added, the `release:version-required` is removed
  - if its a pre-release, the pre-release label is added

## Ref
The composite actions is used from: https://github.com/jpbnetley/release-pr-label-version
