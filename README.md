# Test release pr label version
> release prs with labels

The goal is to add labels to release pr's to indicate what type of release should be applied.  
This follows the [semver](https://semver.org/). IE Major.Minor.Patch.

Once the pr is merged to the release branch (in this case, `main`), the release action will get the last merged pull request,  
and check if any release labels have been added.