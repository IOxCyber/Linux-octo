# Chapter 12. Install and Update Software Packages: `dnf`

## Subscribe a System with the Command Line:
- Simple Content Access (SCA) is a Red Hat subscription management capability.
- `subscription-manager` command to register a system without using a graphical environment.
- Register a system: `subscription-manager register --username <yourusername>`
- View available subscriptions: `subscription-manager list --available`

## Software Packages and RPM:
- The RPM Package Manager provides a way to package software for distribution.
- RPM package file names consist of four elements (plus the .rpm suffix): `name-version-release.architecture`
- ![rpm_name_structure](https://github.com/cybersome/Linux-octo/assets/40174034/d7fd28f4-74e8-49d7-bbfa-b55c4863389b)
- `rpm -qa` : List all installed packages
- `rpm -qf FILENAME` : Determine which package provides FILENAME
- `rpm -q PACKAGE_NAME` : List the currently installed package version
- Install RPM Packages: `rpm -ivh PACKAGE_NAME`


## Manage Software Packages with DNF:
- DNF (Dandified YUM) replaced YUM as the package in RHEL.
- YUM commands still exist as symbolic links to DNF.
- Find Software with DNF: `dnf list 'keyword'` or ` dnf search KEYWORD`
- Install Software: `dnf install PACKAGENAME`
- To displays information: `dnf info PACKAGENAME`
- To update: `dnf upadate 'PACKAGENAME'`
- To remove: `dnf remove 'PACKAGENAME'` First Review the list of packages to be removed.

## Working with Groups:
- Install Groups of Software: `dnf group list`
> To see hidden groups: `dnf group list hidden`
- To displays group information: `dnf group info GROUPNAME`
- To install: `dnf group install GROUPNAME`
- To displays a summary of installation and removal transactions: `dnf history`
- **To reverse a transaction: `dnf history undo NUMBER`**
- <img width="500" alt="image" src="https://github.com/cybersome/Linux-octo/assets/40174034/0f6a5ac3-49eb-4e9e-b42b-3a1bb8a7e5f9">

## Manage Package Module Streams with DNF:
- RHEL distributes the content through two main software repositories: BaseOS and Application Stream (AppStream).
- BaseOS repository provides the core operating system content
- Application Stream repository provides content in both modules and traditional packages.


## Enable Red Hat Software Repositories:
- List all available repositories and their statuses: `dnf repolist all`
- To enable Repo: `dnf config-manager --enable REPO_NAME`
- You can add a third-party repository in one of two ways.
- 1. create a .repo file in the `/etc/yum.repos.d/`
- 2. add a [repository] section to the `/etc/dnf/dnf.conf`
- 







