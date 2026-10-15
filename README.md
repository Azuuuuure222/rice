# Rice

This repository currently stores configuration and utility bundles as archive files in the repository root. Inspect an archive's contents before extracting or applying it.

## Build host vs. target device

This repository does not currently define a software compilation workflow. For binaries produced by related projects, compilation is performed on GitHub Actions; the target device is the machine that runs the resulting binary, not the machine that compiles it.

Target-specific CPU/architecture, libc, display/audio stack, and runtime settings should be reflected in the output binary. The target device's RAM, core count, and storage speed must not be used as reasons to limit CI compilation parallelism. Build concurrency should be based on the actual GitHub Actions runner's available resources and observed build reliability.
