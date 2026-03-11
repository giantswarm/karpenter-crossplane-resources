# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed

- Add `io.giantswarm.application.audience: all` annotation to publish the app to the customer Backstage catalog.
- Migrate chart metadata annotations to `io.giantswarm.application.*` format.

## [0.5.1] - 2025-11-27

### Fixed

- Default the `iam:PassRole` resource to old worker role ARN (the one used before crossplane started managing the IAM Roles) when `workersIamRole` is not provided.

## [0.5.0] - 2025-10-30

### Added

- Add new Helm value to configure the workers IAM role.

[Unreleased]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.5.1...HEAD
[0.5.1]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.5.0...v0.5.1
[0.5.0]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.4.0...v0.5.0
