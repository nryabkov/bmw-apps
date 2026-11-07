# bmw-apps

Personal public app source for MGU Store. The initial catalog is empty and installs nothing.

## Store source

Add `nryabkov/bmw-apps` in Store. The default branch is a valid source through `mgu-repo.json`.

For the Releases channel, publish a non-draft, non-prerelease release tagged `catalog` with `catalog.json` attached as an asset. A catalog committed to the branch alone does not publish the Releases catalog.

This public source can be read without a GitHub account.

## Publishing apps

Publish packages as `<id>@<version>.tgz` with matching package IDs and versions. Add each component to `catalog.json`, including its artifact size and SHA-256, supported `mguHmi`, and any component requirements. Update the catalog asset in the `catalog` release.

For a public repository, artifact URLs use the release download URL; for a private repository, use the GitHub release asset API URL.

Do not publish BMW SDK or firmware-derived code, vehicle identity, diagnostic logs, credentials or private keys.

Format reference: [MGU Store publishing guide](https://github.com/robertnisipeanu/mgu-store/blob/main/docs/PUBLISHING.md).
