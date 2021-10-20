# Repo Has Moved

This repo has moved to https://github.com/kronicle-tech/kronicle-metadata-repo-template


# Component Metadata Template

This repo contains a template for creating new `component-metadata` repos.

## Creating a new `component-metadata` repo

When adding a team and/or area to the Component Catalog, you will need a `component-metadata` repo.

Here are the steps to create a new `component-metadata` repo.  You should **NOT** create the following
repo by forking this repo.  Instead you should follow these steps to create a brand new repo that
contains a copy of the code from this template repo:

1. Run these steps:
   
   ```shell
   $ mkdir example
   $ cd example
   $ git clone https://github.com/moneysupermarket/component-metadata-repo-template.git component-metadata
   $ cd component-metadata
   $ rm -rf .git/
   $ rm README.md
   $ mv README-example.md README.md
   $ git init
   $ git add --all
   $ git commit -m "Initial commit"
   # Replace URL with the URL of your new repo 
   $ git remote add origin https://example.com/component-metadata.git
   $ git push -u origin HEAD:main
   ```
   
3. Replace references to `EXAMPLE`, `Example` and `example` in the following files:
   * [README.md](README.md)
   * [component-metadata.yaml](component-metadata.yaml)
4. Replace the areas, teams and components in the [component-metadata.yaml](component-metadata.yaml) file.
5. Raise a PR to commit your changes to the new repo

## Adding areas, teams and components to the repo

See the [component-metadata.yaml](component-metadata.yaml) file for example YAML for areas, teams and components.
Here's a description of those concepts: 

* An area is any grouping of 1 or more teams. It could be a company vertical or any other sort of organisational unit.
* A team is typically a single product engineering team or other team.
* A component could be web frontend, mobile app, microservice, database, queue, a CDN or any other type of software or
 infrastructure.

The [component-metadata.yaml](component-metadata.yaml) file can contain any number of areas, teams and components,
include none of each of them.

Typically, a `component-metadata` repo will contain team(s) and/or area(s).

Components can also be defined in that repo. Alternatively, each component can be defined in a `component-metadata.yaml`
file in the component's own repo.

## Changes to `component-metadata.yaml` files just need to be merged to main branch

The Component Catalog automatically scans for any repos with a `component-metadata.yaml` file at the
root of the repo.  If you create a `component-metadata.yaml` file in a `component-metadata` repo or in a component's own
codebase repo, the Component Catalog will automatically pick up the file and any changes made to it.  The Component Catalog
scans all repos every 15 minutes.  Any changes to a `component-metadata.yaml` file that are merged to the main branch 
should be detected and loaded by the Component Catalog in 15 to 30 minutes.  
