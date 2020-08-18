# lgtm

`lgtm` plugin documentation:
- [Description](#description)
- [Commands](#commands)
- [Configuration](#configuration)
- [Compatibility matrix](#compatibility-matrix)

## Description

The lgtm plugin manages the application and removal of the `lgtm` (looks good to me) label which is typically used to gate merging.

## Commands

### /lgtm or /lh-lgtm

The `/lgtm` or `/lh-lgtm` commands add the `lgtm` label to a pull request.

### /lgtm cancel or /lh-lgtm cancel

The `/lgtm cancel` or `/lh-lgtm cancel` commands remove the `lgtm` label to a pull request.

## Configuration

### Configuration stanza

| stanza    | type                       |
| --------- | -------------------------- |
| `lgtm`    | [][Lgtm](#lgtm-type)         |

### Lgtm type

| field   | type     | note                                                 | default value |
| ------- | -------- | ---------------------------------------------------- | ------------- |
| `s`     | int      | number of lines of changes to apply the `s` size     | 10            |
| `m`     | int      | number of lines of changes to apply the `m` size     | 30            |
| `l`     | int      | number of lines of changes to apply the `l` size     | 100           |
| `xl`    | int      | number of lines of changes to apply the `xl` size    | 500           |
| `xxl`   | int      | number of lines of changes to apply the `xxl` size   | 1000          |

## Compatibility matrix

|               | GitHub | GitHub Enterprise | BitBucket Server | GitLab |
| ------------- | ------ | ----------------- | ---------------- | ------ |
| Pull requests | Yes    | Yes               | Yes              | Yes    |
| Commits       | No     | No                | No               | No     |
