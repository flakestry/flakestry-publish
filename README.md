## [Publish a flake to flakestry.dev](https://flakestry.dev/publish)

### Inputs

- `url`: defaults to `https://flakestry.dev`
- `ref`: a git reference — such as `HEAD`, `refs/heads/main`, or
  `refs/tags/v1.0.0` —, or a full commit hash. Defaults to the hash of the
  commit that triggered this action.
- `version`: should be a [semver](https://semver.org/). If not provided, it
  defaults to either the tag (if the given reference is a tag) or the UTC commit
  date otherwise, in the format `v0.1.yyyymmddHHMMSS`.
- `ignoreConflicts`: by default, if the version already exists this action will
  fail. Set this to true to silently ignore it instead. Note that this will not
  force an override of the version already present, just silence the error.
