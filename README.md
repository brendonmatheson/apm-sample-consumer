# APM Sample Consumer

A minimal consumer for the GitHub-hosted
[`brendonmatheson/apm-sample-package`](https://github.com/brendonmatheson/apm-sample-package).
The dependency and its current release pin are declared in `apm.yml`.

## Import the package

Install the declared dependency from this directory:

```bash
apm install
```

APM resolves the producer package and generates a lockfile and runtime files for
the configured target.

## Upgrade the dependency

When the producer publishes a new release, update its version pin in `apm.yml`
(for example, `#v1.0.0` to `#v1.0.1`), then run:

```bash
apm install
```

Review the updated lockfile and installed package files along with the manifest
change. The manifest pin is the consumer's requested version; the lockfile
records the exact resolved package revision.
