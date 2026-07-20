# Scaleweave

Scaleweave is an unofficial Gentoo ebuild repository for Prismdrake, Glasswyrm, and related draconic software projects.

> [!NOTE]
> The repository is currently being bootstrapped. Packages will be added as the associated projects become ready for distribution.

## Adding the repository

Install the repository-management tooling if it is not already available:

```bash
emerge --ask --noreplace app-eselect/eselect-repository dev-vcs/git
```

Add Scaleweave and synchronize it:

```bash
eselect repository add scaleweave git https://github.com/JTM-rootstorm/scaleweave-overlay.git
emaint sync -r scaleweave
```

Alternatively, configure Portage directly with `/etc/portage/repos.conf/scaleweave.conf`:

```ini
[scaleweave]
location = /var/db/repos/scaleweave
sync-type = git
sync-uri = https://github.com/JTM-rootstorm/scaleweave-overlay.git
auto-sync = yes
```

Then synchronize the repository:

```bash
emaint sync -r scaleweave
```

## Repository scope

Scaleweave is intended to host Gentoo packaging for:

- Prismdrake Desktop Environment and its components
- Glasswyrm and its related components
- Shared libraries, tools, themes, and supporting packages used by the wider project family

Package-specific installation and configuration instructions will be added alongside the packages that require them.

## Repository structure

Scaleweave follows the standard Gentoo ebuild repository layout and inherits from the main `gentoo` repository. Package categories will be introduced as packages are added.

## Status

Early bootstrap. No packages are currently published.
