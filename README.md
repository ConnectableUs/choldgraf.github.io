# Connectable.Us website, cloned from Chris Holdgraf's personal site configuration

This is Connectable.Us website, built with Sphinx!

I'm starting by making small modification to Chris's repository here, to provide
my own template for the four blogs described in the branches (connectable, thynken,
yarko, ingeniere).


## Build and preview the docs

**Build the docs**. Use `nox`, which handles all of the environment generation automatically.
To do so, follow these steps:

1. Install `nox`.

   ```shell
   pip install -U nox
   ```
2. Run `tox`

   ```shell
   nox -s docs
   ```
This should install a Sphinx environment and build the site, putting the output files in `_build/html`.

To view the files from the output directory, use `python -m https.server`  (will display on `localhost:8000`),
or view live, as shown next.


## Execute and interact with the code

**Run a live webserver**:

```shell
nox -s docs -- live
```

**Run a JupyterLab environment with necessary packages installed:

```shell
nox -s lab
```

## Update my publications

The script in `scripts/orcid-publications.py` will use [the ORCID APi](https://info.orcid.org/documentation/api-tutorials/api-tutorial-read-data-on-a-record/) to download all of the records associated with my ORCID account.

It generates some markdown that is then inserted into my documentation in `publications.md`.
