# salcode GitHub CLI Configuration

My configuration for GitHub CLI and notes.

## Aliases

### `gh redeliver <PR URL>`

Based on the PR URL (e.g. `https://github.com/salcode/my-example-repo/pull/23`) find the most recent webhook delivery (for the first webhook defined for the repo (`salcode/my-example-repo`)) where:

- the `action` has a value of `closed`
- the `event` has a value of `pull_request`
- the Pull Request ID (`.request.payload.number`) matches the Pull Request Number in the URL

e.g. `gh redeliver https://github.com/salcode/my-example-repo/pull/23`

## Setup

Clone this repo (e.g. in your home directory)

```
git clone git@github.com:salcode/salcode-gh-cli.git ~/salcode-gh-cli.git
```

Symlink your the `config.yml` in this repo to the GitHub CLI config file location (`~/.config/gh/config.yml`)

```
ln -sf ~/salcode-gh-cli/config.yml ~/.config/gh/config.yml`
```
