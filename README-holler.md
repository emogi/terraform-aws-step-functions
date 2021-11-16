# Holler README
This is a fork of the [terraform-aws-modules/terraform-aws-step-functions](https://github.com/terraform-aws-modules/terraform-aws-step-functions) repository. To work on this repo, do the following.

1. Clone this repo: `git clone git@github.com:emogi/terraform-aws-step-functions.git`
1. Add upstream repo: `git remote add --track master upstream git@github.com:terraform-aws-modules/terraform-aws-step-functions.git`

I have created a `holler` branch as follows.

```
git checkout -b holler v2.5.0
```

We will tag our releases based on the upstream version on which we base our changes. For example

```
vim whatever.tf
git commit
git push
git tag -a v2.5.0-holler
```
