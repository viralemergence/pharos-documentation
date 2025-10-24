[![Pharos](https://github.com/viralemergence/pharos-database/blob/prod/img/pharos-banner.png)](https://pharos.viralemergence.org/)

This repository is part of the [Pharos project](https://pharos.viralemergence.org/)
which is split into three repositories:

| Repository                                                                       | Purpose                                            |
| -------------------------------------------------------------------------------- | -------------------------------------------------- |
| [`pharos-frontend`](https://github.com/viralemergence/pharos-frontend)           | Frontend application and deployment infrastructure |
| [`pharos-api`](https://github.com/viralemergence/pharos-api)                     | API and deployment infrastructure                  |
| [`pharos-database`](https://github.com/viralemergence/pharos-database)           | SQL database and deployment infrastructure         |
| [`pharos-documentation`](https://github.com/viralemergence/pharos-documentation) | Markdown files used to generate about pages        |

</br>
</br>
</br>
<h1 align="center">
  Pharos Documentation
</h1>

## 🚀 Deployment Status

CI/CD deployments are not triggered by any changes in this repository, deployments of all
content in the `publish` bransh of this repository occur when changes are pushed or builds
are triggered in the [`pharos-frontend`](https://github.com/viralemergence/pharos-frontend)
repository.

| Branch  | CI/CD Status                                                                                                                                                                                                                                                 | Url                                                                              |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------- |
| Prod    | [![CircleCI](https://dl.circleci.com/status-badge/img/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/prod.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/prod)       | [pharos.viralemergence.org/](https://pharos.viralemergence.org/)                 |
| Staging | [![CircleCI](https://dl.circleci.com/status-badge/img/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/staging.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/staging) | [staging-pharos.viralemergence.org/](https://staging-pharos.viralemergence.org/) |
| Review  | [![CircleCI](https://dl.circleci.com/status-badge/img/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/review.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/review)   | [dev-pharos.viralemergence.org/](https://review-pharos.viralemergence.org/)      |
| Dev     | [![CircleCI](https://dl.circleci.com/status-badge/img/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/dev.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/circleci/39PL8myokkHY7obZPJeFEC/VSEyuiVS42F6DmyCLZcbdW/tree/dev)         | [dev-pharos.viralemergence.org/](https://dev-pharos.viralemergence.org/)         |

Automated deployment schedule: AirtableCMS data is ingested, "About" content is ingested, and full site is built weekly on `Staging` site.

</br>

## 👩‍💻 Overview

This repository contains the markdown files which are used to create the
[`/about/` pages](https://pharos.viralemergence.org/about/) on
[pharos.viralemergence.org/about/](https://pharos.viralemergence.org/about/).

These pages contain documentation, instructions, user agreements, and other
content to help users.

## To contribute a documentation change:

1. Team members with access may push changes to the `main` branch
1. Contributors outside the core team may create a fork, and open a PR to this repository
1. PR with changes should be made against the `publish` branch
1. Once approved and merged, the documentation changes will show up on the `staging` site during the next automatic build
1. To push changes to the `prod` site, a team member with appropriate permissions should trigger a build in [`pharos-frontend`](https://github.com/viralemergence/pharos-frontend).

</br>

## Markdown

Quick help with Markdown formatting syntax can be found on
the [Commonmark help page](https://commonmark.org/help/).

The full
[commonmark spec can be found here](https://spec.commonmark.org/0.30/).

</br>

## Directory, File and Page Structure

The directory structure in this repository maps to the
sidebar and page structure of the site. Pages created in
this project will be transformed into pages, using the
name of the file as the url; for example `about.md` becomes
[https://pharos.viralemergence.org/about/](https://pharos.viralemergence.org/about/).

When files are in directories, such as `/guide-for-users/`,
then the metadata from the readme file is used to create
a section in the sidebar which links to the url based on
the directory name.

### Frontmatter:

Metadata for documentation pages is pulled from the
"frontmatter" which is the small section demarcated by
three hyphens `---` at the top of each markdown file.

We support two frontmatter fields:

#### `title`

This field sets the title of the generated page and the
link text for the sidebar link which points to it.

#### `order`

This field sets the sidebar order of the page, relative
to its section (directory) The `order` field from the
`README.md` file in each directory sets the order of the
section in the parent list.

</br>

## Linking

_Files in this repository should not be renamed now that
the site is live, because it will break internal links
(which we can fix) and external links and SEO (which we
cannot fix)_. If renaming a file is extremely important,
please reach out to
[ryan.zimmerman@georgetown.edu](mailto:ryan.zimmerman@georgetown.edu).

There are two types of links which must be handled
separately; internal links to other pages on pharos, and
external links to other websites.

Incorrect links confuse users and damage SEO (How Google
ranks Pharos in their results) so it is important for
links to be correct and maintained.

### Internal links (Links to Pharos pages)

To link to a page on the Pharos site, you need to only
use the path, not the entire link.

For example, to link to the user agreement page at
`https://pharos.viralemergence.org/user-agreement/`
you need to take just the last part of the link, after
the `.org`: just `/user-agreement/`.

The link should look like this in markdown:

`[user agreement](/user-agreement/)`

### External links (links to non-Pharos sites)

To link outside the pharos site, it is important to
include the full and complete link, including the
`https://` in the beginning.

For example, to link to [example.org](https://example.org),
the link in markdown should look like this:

`[example.org](http://example.org)`.

If the `https://` is ommitted from the front of the
link, it will be interpreted as an internal link.

### Email links

To add an email address into a documentation page, you
should create a `mailto` link like this:

`[ryan.zimmerman@georgetown.edu](mailto:ryan.zimmerman@georgetown.edu?subject=Example)`

This syntax will render like this:

[ryan.zimmerman@georgetown.edu](mailto:ryan.zimmerman@georgetown.edu?subject=Example)

Clicking the link will open the user's default email
program and will fill in the subject line with the
text after the `?subject=` section of the
link if it is provided (optional!).

</br>

## Under the hood

Markdown files in this repository are parsed using
[micromark](https://github.com/micromark/micromark) which
is compliant with
[the commonmark standard](https://commonmark.org/help/) so
commonmark documentation should be used as the reference
for markdown syntax in this project.

The full
[commonmark spec can be found here](https://spec.commonmark.org/0.30/).
