1. Update version in package.json and commit version bump.
2. Merge PR into master (not mandatory for alpha-releases).
3. Run `yarn publish --tag alpha`. Don't enter new version since you updated it manually before. Project build command will be called before publishing (see _prepublishOnly_ script).