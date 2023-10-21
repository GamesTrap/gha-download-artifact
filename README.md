# Download artifact

Download an artifact (7z file) from a Samba server and unpack it.

## Example usage

```yaml
- uses: GamesTrap/gha-download-artifact
  with:
    server-hostname: <Server IP/Domain>
    server-share: <Samba share>
    server-username: <Samba username>
    server-password: <Samba password>
    artifact-name: <Name of artifact to download>
```

## Inputs

### `server-hostname`

Set this to the server ip/domain of the samba server, for example: `127.0.0.1`

### `server-share`

Set this to the samba share path, for example: `myshare\mydata\artifacts`

### `server-username`

Set this to the username to be used as login for samba

### `server-password`

Set this to the password to be used as login for samba  

**Note: Make sure to use a [secret](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions) for the password!**

### `artifact-name`

Set this to the name of the artifact to download. The action will automagically figure out the correct artifact to download using data like the repository name, branch name, commit hash and so on...
