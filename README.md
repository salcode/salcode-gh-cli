# salcode GitHub CLI Configuration

My configuration for GitHub CLI and notes.

## Aliases

### `gh redeliver <webhook payload URL>`

Based on the webhook payload URL (e.g. `https://example.com/dev/hook`) resend the most recent webhook delivery to that URL that meets the criteria:

- the `action` has a value of `closed`
- the `event` has a value of `pull_request`

e.g. `gh redeliver https://example.com/dev/hook`

**Note**: Your current branch has no impact on which webhook delivery is resent.

## Setup

Clone this repo (e.g. in your home directory)

```
git clone git@github.com:salcode/salcode-gh-cli.git ~/salcode-gh-cli.git
```

Symlink your the `config.yml` in this repo to the GitHub CLI config file location (`~/.config/gh/config.yml`)

```
ln -sf ~/salcode-gh-cli/config.yml ~/.config/gh/config.yml`
```
