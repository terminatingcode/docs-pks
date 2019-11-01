# Enterprise Pivotal Container Service (Enterprise PKS) Documentation

This repository contains the content for the documentation for Enterprise Pivotal Container Service
(Enterprise PKS).

The content in this repository publishes to the Enterprise PKS documentation site at
https://docs.pivotal.io/pks/index.html.

## How To Contribute

Please help us improve the accuracy and completeness of the Enterprise PKS documentation by
contributing.

The easiest way to contribute is to file a pull request through GitHub.

Every topic in the [Enterprise PKS documentation site](https://docs.pivotal.io/pks/index.html) has
a corresponding file in this repository. Locate the correct file and make a pull request against
it. You can also navigate to the topic in the Enterprise PKS documentation site and click "View the
source for this page in GitHub" at the bottom of the topic to locate the source file of a topic.

## Versions and Branching

| **Branch Name** | **Content** | **Location** |
|-----------------|-------------|--------------|
| `1.6` | Enterprise PKS 1.6 pre-release content | https://docs.pivotal.io/pks/1-6/index.html |
| `1.5` | Enterprise PKS 1.5 released content    | https://docs.pivotal.io/pks/1-5/index.html |
| `1.4` | Enterprise PKS 1.4 released content    | https://docs.pivotal.io/pks/1-4/index.html |
| `1.3` | Enterprise PKS 1.3 released content    | https://docs.pivotal.io/pks/1-3/index.html |
| `1.2` | Not in use | N/A ([PDF available](https://resources.docs.pivotal.io/pdfs/pks-1-2.pdf)) |
| `1.1` | Not in use | N/A ([PDF available](https://resources.docs.pivotal.io/pdfs/pks-1-1.pdf)) |
| `1.0-publish` | Not in use | N/A ([PDF available](https://resources.docs.pivotal.io/pdfs/pks-docs-1.0.pdf)) |
| `0.8` | Not in use | N/A|
| `pks-patches` | Staging site for not-yet-released Enterprise PKS patches. | Publishes to an internal staging site only. |

**1.6**: The `1.6` branch is used to publish the pre-release v1.6 version of the site. Create pull requests on `1.6` to contribute bug fixes or correct technical inaccuracies in the pre-release v1.6 documentation.

**1.5**: The `1.5` branch is used to publish the live v1.5 version of the site. Create pull requests on `1.5` to contribute bug fixes or correct technical inaccuracies in the v1.5 documentation.

**1.5.x-patch-releases**: The `1.5.x-patch-releases` branch is used to publish the 1.5 site including information included for unreleased patches. Create pull requests on `1.5.x-patch-releases` to contribute to documentation for unreleased 1.5 patches.

**1.4**: The `1.4` branch is used to publish the live v1.4 version of the site. Create pull requests on `1.3` to contribute bug fixes or correct technical inaccuracies in the v1.4 documentation.

**1.4.x-patch-releases**: The `1.4.x-patch-releases` branch is used to publish the 1.4 site including information included for unreleased patches. Create pull requests on `1.4.x-patch-releases` to contribute to documentation for unreleased 1.4 patches.

**1.3**: The `1.3` branch is used to publish the live v1.3 version of the site. Create pull requests on `1.3` to contribute bug fixes or correct technical inaccuracies in the v1.3 documentation.

**1.3.x-patch-releases**: The `1.3.x-patch-releases` branch is used to publish the 1.3 site including information included for unreleased patches. Create pull requests on `1.3.x-patch-releases` to contribute to documentation for unreleased 1.3 patches.

The `1.2` branch is no longer maintained. A PDF of the Enterprise PKS v1.2 documentation is available at https://resources.docs.pivotal.io/pdfs/pks-docs-1.2.pdf.

The `1.1` branch is no longer maintained. A PDF of the Enterprise PKS v1.1 documentation is available at https://resources.docs.pivotal.io/pdfs/pks-docs-1.1.pdf.

The `1.0-publish` and `0.8` branches are no longer maintained. A PDF of the Enterprise PKS v1.0 documentation is available at https://resources.docs.pivotal.io/pdfs/pks-docs-1.0.pdf.

## How To Use Bookbinder To View Your Documentation

[Bookbinder](https://github.com/pivotal-cf/bookbinder/blob/master/README.md) is a command-line
utility for stitching Markdown documents into a hostable web app. The documentation team uses
Bookbinder to publish our documentation sites, but you can also use Bookbinder to view a live
version of your documentation on your local machine.

Bookbinder draws the content for the site from this repository, the left navigation menu ("subnav")
from [`docs-book-pks`](https://github.com/pivotal-cf/docs-book-pks), and various layout
configuration and assets from [`docs-layout-repo`](https://github.com/pivotal-cf/docs-layout-repo).

To use Bookbinder to view your documentation, perform the following steps:

1. Clone this repository to the `~/workspace` directory on your local machine.
1. Clone [`docs-book-pks`](https://github.com/pivotal-cf/docs-book-pks) and [`docs-layout-repo`](https://github.com/pivotal-cf/docs-layout-repo) to the `~/workspace` directory on your local machine.
1. Navigate into the `docs-book-pks` directory.
1. Run `bundle install` to install all of the necessary gems, including Bookbinder.
1. Run `bundle exec bookbinder bind local` to build a Rack web-app of the book. After the bind has completed, navigate into the `final_app` directory and run `rackup`. Then navigate to `localhost:9292/pks/1-6/index.html` in a browser.
