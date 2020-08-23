# repo-procedures
Checklists for repo management.

## Repo Creation

## CI Set Up

## Publish Version

- [ ] Update version numbers of all crates.
- [ ] Update in-crate documentation
- [ ] Run `cargo readme -o README.md` then correct doc links and whitespace.
- [ ] Update CHANGELOG.md
  - [ ] Move all unreleased changes into section with new version.
  - [ ] Add any missing changes. Use sections from [https://keepachangelog.com/en/1.0.0/](keepachangelog.com).
  - [ ] First thing in version section is: `Released YYYY-MM-DD`
  - [ ] Update diffs to include section from `<old-version>..<new-version>`
  - [ ] Update unreleased diff to `<new-version>..HEAD`
- [ ] Commit all changes and merge into `master` if needed
- [ ] Create a tag on `master` commit with full version info: `v0.6.0`.
- [ ] Push tag to github
- [ ] Create github release on that tag
  - [ ] Named `v0.6.0` or `v0.6.0 - Optional Quick Summary of Changes`.
  - [ ] Copy changelog for release into body of gh release.
- [ ] Run through checklist again
- [ ] `cargo workspace publish` or series of `cargo publish`
