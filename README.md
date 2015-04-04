# test-github-release
Test repo for creating and testing GitHub releases from fully automated process


Here I found some useful details on how to create a release from an externel CLI command: http://www.barrykooij.com/create-github-releases-via-command-line/.


## Step 1: generate a new GitHub access token
see: https://help.github.com/articles/creating-an-access-token-for-command-line-use/

Name=CLI-Test GitHub Releases
- [x] public_repo

```bash
export GITHUB_TOKEN=xxx
```

## Step 2: create a new release with `curl`
```bash
curl --data '{"tag_name": "v0.1.0","target_commitish": "master","name": "v0.1.0","body": "Release of version 0.1.0","draft": false,"prerelease": false}' https://api.github.com/repos/dieterreuter/test-github-release/releases?access_token=$GITHUB_TOKEN
```

```bash
curl --data '{"tag_name": "v0.2.0","target_commitish": "master","name": "v0.2.0","body": "Release of version 0.2.0\n\nxxx","draft": false,"prerelease": false}' https://api.github.com/repos/dieterreuter/test-github-release/releases?access_token=$GITHUB_TOKEN
```

```bash
curl --data '{"tag_name": "v0.3.0","target_commitish": "master","name": "v0.3.0","body": "Release of version 0.3.0\n\n[Docker 1.6.0-rc4 for Raspberry Pi](http://assets.hypriot.com/docker-hypriot_1.6.0-rc4-1_armhf.deb) [sha256sum](http://assets.hypriot.com/docker-hypriot_1.6.0-rc4-1_armhf.deb.sha256)","draft": false,"prerelease": false}' https://api.github.com/repos/dieterreuter/test-github-release/releases?access_token=$GITHUB_TOKEN
```
