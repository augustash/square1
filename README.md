# Square1 Distribution

Square1 is a Starter Kit distribution and installation profile to be used as an alternative to `minimal` or `standard` when installing a Drupal 8 website. It contains improvements over the `standard` installation profile by enabling helpful modules, configuring default settings, and including a base theme to facilitate building Drupal websites faster.

**This repository is not currently aimed at public consumption. It exists as a starting point for [August Ash](https://www.augustash.com/) made [Drupal](https://www.drupal.org/) projects built on [Pantheon](https://pantheon.io/).**

## Usage

To add Square1 to your Pantheon repository, follow the below steps:

1) Clone a newly created Pantheon Site's repository:

```
git clone ssh://codeserver.dev.12345678-1234-1234-1234-ab1234567890@codeserver.dev.12345678-1234-1234-1234-ab1234567890.drush.in:2222/~/repository.git new_project
```

2) Merge Square1 code changes into your Pantheon repository:

```
cd new_project/
git pull git@github.com:augustash/square1.git master
```

3) Install Square1 dependencies:

```
composer install
```

4) Push merged changes back to Pantheon

```
git push origin master
```

5) Put the Pantheon site into SFTP during installation, and visit the install page, `/core/install.php`, to complete the process.

## Merge Upstream Changes

This repository is a fork of [Pantheon's Drops-8 repository](https://github.com/pantheon-systems/drops-8). As they update their codebase, the changes should be merged into Square1. Follow this process to merge upstream changes:

1) Clone the Square1 repository:

```
git clone git@github.com:augustash/square1.git square1
cd square1/
```

2) Add Pantheon's repository as an upstream Git remote:

```
git add remote upstream git@github.com:pantheon-systems/drops-8.git
```

3) Fetch any branches and their commits from the upstream repository:

```
git fetch upstream
```

4) Check out the Square1 `master` branch:

```
git checkout master
```

5) Merge commits from `upstream/master` to Square1's `master` branch:

```
git merge upstream/master
```

**Note:** You may run into merge conflicts with `composer.lock` and the `vendor` directory in particular. The easiest solution is to remove `composer.lock` and the full `vendor` directory, then run `composer install`. You can then safely add the new/changed items and complete the merge commit. More specific help can be found in [Github's Upstream Article](https://help.github.com/articles/syncing-a-fork/).
