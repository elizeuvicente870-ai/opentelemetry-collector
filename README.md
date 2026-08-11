---

<p align="center">
  <strong>
    <a href="https://opentelemetry.io/docs/collector/getting-started/">Getting Started</a>
    &nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="CONTRIBUTING.md">Getting Involved</a>
    &nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://cloud-native.slack.com/archives/C01N6P7KR6W">Getting In Touch</a>
  </strong>
</p>

<p align="center">
  <a href="https://github.com/open-telemetry/opentelemetry-collector/actions/workflows/build-and-test.yml?query=branch%3Amain">
    <img alt="Build Status" src="https://img.shields.io/github/actions/workflow/status/open-telemetry/opentelemetry-collector/build-and-test.yml?branch=main&style=for-the-badge">
  </a>
  <a href="https://codecov.io/gh/open-telemetry/opentelemetry-collector/branch/main/">
    <img alt="Codecov Status" src="https://img.shields.io/codecov/c/github/open-telemetry/opentelemetry-collector?style=for-the-badge">
  </a>
  <a href="https://github.com/open-telemetry/opentelemetry-collector/releases">
    <img alt="GitHub release (latest by date including pre-releases)" src="https://img.shields.io/github/v/release/open-telemetry/opentelemetry-collector?include_prereleases&style=for-the-badge">
  </a>
  </br>
  <a href="https://www.bestpractices.dev/projects/8404"><img src="https://www.bestpractices.dev/projects/8404/badge">
  </a>
  <a href="https://bugs.chromium.org/p/oss-fuzz/issues/list?sort=-opened&can=1&q=proj:opentelemetry">
    <img alt="Fuzzing Status" src="https://oss-fuzz-build-logs.storage.googleapis.com/badges/opentelemetry.svg">
  </a>
</p>

<p align="center">
  <strong>
    <a href="docs/vision.md">Vision</a>
    &nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://opentelemetry.io/docs/collector/configuration/">Configuration</a>
    &nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://opentelemetry.io/docs/collector/internal-telemetry/#use-internal-telemetry-to-monitor-the-collector">Monitoring</a>
    &nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="docs/security-best-practices.md">Security</a>
    &nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://pkg.go.dev/go.opentelemetry.io/collector">Package</a>
  </strong>
</p>

---

# <img src="https://opentelemetry.io/img/logos/opentelemetry-logo-nav.png" alt="OpenTelemetry Icon" width="45" height=""> OpenTelemetry Collector

The OpenTelemetry Collector offers a vendor-agnostic implementation on how to
receive, process and export telemetry data. In addition, it removes the need
to run, operate and maintain multiple agents/collectors in order to support
open-source telemetry data formats (e.g. Jaeger, Prometheus, etc.) to
multiple open-source or commercial back-ends.

Objectives:

- Usable: Reasonable default configuration, supports popular protocols, runs and collects out of the box.
- Performant: Highly stable and performant under varying loads and configurations.
- Observable: An exemplar of an observable service.
- Extensible: Customizable without touching the core code.
- Unified: Single codebase, deployable as an agent or collector with support for traces, metrics and logs.


- meet the humans behind the project
- get an opinion about specific proposals
- look for a sponsor for a proposed component after trying already via GitHub and Slack
- get attention to a specific pull-request that got stuck and is difficult to discuss asynchronously

We rotate our video calls between three time slots, in order to
allow everyone to join at least once every three meetings. The rotation order is as follows:


Contributors to the project are also welcome to have ad-hoc meetings for synchronous discussions about specific points.
Post a note in #otel-collector-dev on Slack inviting others, specifying the topic to be discussed. Unless there are strong
reasons to keep the meeting private, please make it an open invitation for other contributors to join. Try also to
identify who would be the other contributors interested on that topic and in which timezones they are.

Remember that our source of truth is GitHub: every decision made via Slack or video calls has to be recorded in the
relevant GitHub issue. Ideally, the agenda items from the meeting notes would include a link to the issue or pull
request where a discussion is happening already. We acknowledge that not everyone can join Slack or the synchronous
calls and don't want them to feel excluded.


This code base is currently built against using OTLP protocol v1.10.0,
considered Stable. [See the OpenTelemetry 
Removing support for an unsupported Go version is not considered a breaking change.

Support for Go versions on the OpenTelemetry Collector is updated as follows:

1. The first release after the release of a new Go minor version `N` will add build and tests steps for the new Go minor version.
2. The first release after the release of a new Go minor version `N` will remove support for Go version `N-2`.

Within supported Go minor versions, the minimum supported patch version may increase over time, for example to accommodate dependency updates. Increasing the minimum supported patch version within a supported Go minor version is not considered a breaking change.

Official OpenTelemetry Collector distro binaries will be built with a release in the latest Go minor version serie




```console
$ cosign verify --certificate-identity=https://github.com/open-telemetry/opentelemetry-collector-releases/.github/workflows/base-release.yaml@refs/tags/v0.98.0 --certificate-oidc-issuer=https://token.actions.githubusercontent.com ghcr.io/open-telemetry/opentelemetry-collector-releases/opentelemetry-collector-contrib:0.98.0

Verification for ghcr.io/open-telemetry/opentelemetry-collector-releases/opentelemetry-collector-contrib:0.98.0 --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - The code-signing certificate was verified using trusted certificate authority certificates

