# Holler Notes
This is a fork of the [terraform-aws-modules/terraform-aws-step-functions](https://github.com/terraform-aws-modules/terraform-aws-step-functions) repository. This is a **PUBLIC REPOSITORY** and all branches, commit messages, pull requests, etc, are public. Keep this in mind as you work on this repo.


To work on this repo, do the following.

```
git clone git@github.com:emogi/terraform-aws-step-functions.git
git remote add --track master upstream git@github.com:terraform-aws-modules/terraform-aws-step-functions.git
```

We will tag our releases based on the upstream version on which we base our changes. For example,

```
git checkout -b feature_branch ${upstream_version}-holler-${holler_version}
vim whatever.tf
git commit
git push -u origin feature_branch

# Approve & merge PR then
git checkout master
git pull
git tag -a ${upstream_version}-holler-${holler_version}
```

## CHANGELOG
* 2021-11-16: Add `lifecycle` rule to resource `aws_sfn_state_machine.this`, ignoring changes to the `definitions` variable. This change cannot be pushed upstream because terraform does not support dynamic blocks for lifecycle rules, nor does terraform support variables inside a lifecycle rule ([issue](https://github.com/hashicorp/terraform/issues/3116))
