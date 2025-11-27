# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.5.1] - 2025-11-27

### Fixed

- Default the `iam:PassRole` resource to old worker role ARN (the one used before crossplane started managing the IAM Roles) when `workersIamRole` is not provided. This is needed to make our tests automation to work, regardless of the version of this app used.

## [0.5.0] - 2025-10-30

### Added

- Add new Helm value to configure the workers IAM role. When Karpenter launches worker instances, it will attach the worker instance profile.
  To do that, AWS requires that the calling role (Karpenter’s role) have the `iam:PassRole` permission for the worker role being attached.
  This prevents privilege escalation as you can’t make EC2s with arbitrary roles unless you’re explicitly allowed to pass them.

## [0.4.0] - 2025-10-02

### Changed

- Add `iam:ListInstanceProfiles` for release 1.7.1


## [0.3.0] - 2025-10-02

### Added

- Add `giantswarm.io/managed-by` tag to AWS Resources.


## [0.2.1] - 2025-09-11

### Fixed

- Remove duplicated labels

## [0.2.0] - 2025-09-11

### Changed

- Move to default catalog

## [0.1.4] - 2025-04-10

### Added

- Included the `giantswarm.io/cluster` label

## [0.1.3] - 2024-10-04

### Changed

- Make use of the new `oidcDomains` value in the crossplane info ConfigMap, remove use of internal value

## [0.1.2] - 2024-09-05

### Changed

- Add support for vintage OIDC issuer for migrated clusters

## [0.1.1] - 2024-05-09

### Fixed

- SQS Selector

## [0.1.0] - 2024-04-29

## [0.0.7] - 2024-04-25

### Changed

- Use OIDC Domain parameter

## [0.0.6] - 2024-03-18

### Fixed

- Fix IRSA URL in the IAM role.

## [0.0.5] - 2024-02-06

## [0.0.4] - 2024-02-06

## [0.0.3] - 2024-02-06

## [0.0.2] - 2024-02-06

## [0.0.1] - 2024-02-02

[Unreleased]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.5.1...HEAD
[0.5.1]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.5.0...v0.5.1
[0.5.0]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.2.1...v0.3.0
[0.2.1]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.1.4...v0.2.0
[0.1.4]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.1.3...v0.1.4
[0.1.3]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.1.2...v0.1.3
[0.1.2]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.1.1...v0.1.2
[0.1.1]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.7...v0.1.0
[0.0.7]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.6...v0.0.7
[0.0.6]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.5...v0.0.6
[0.0.5]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.4...v0.0.5
[0.0.4]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.3...v0.0.4
[0.0.3]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.2...v0.0.3
[0.0.2]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.1...v0.0.2
[0.0.1]: https://github.com/giantswarm/karpenter-crossplane-resources/compare/v0.0.1...v0.0.1
