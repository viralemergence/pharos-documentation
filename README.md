# pharos-documentation

## Markdown

Quick help with Markdown formatting syntax can be found on
the [Commonmark help page](https://commonmark.org/help/).

The full
[commonmark spec can be found here](https://spec.commonmark.org/0.30/).


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

## Linking

*Files in this repository should not be renamed now that
the site is live, because it will break internal links
(which we can fix) and external links and SEO (which we
cannot fix)*. If renaming a file is extremely important,
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

## Under the hood

Markdown files in this repository are parsed using
[micromark](https://github.com/micromark/micromark) which
is compliant with
[the commonmark standard](https://commonmark.org/help/) so
commonmark documentation should be used as the reference
for markdown syntax in this project.

The full
[commonmark spec can be found here](https://spec.commonmark.org/0.30/).
