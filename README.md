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
