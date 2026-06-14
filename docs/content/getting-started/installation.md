---
title: "Installation"
description: "Install ronswanson from a release, with go install, or from source."
weight: 20
---

## Prebuilt binaries

Every [release](https://github.com/tamnd/ronswanson-cli/releases) carries archives for Linux, macOS,
and Windows on amd64 and arm64, plus deb, rpm, and apk packages for Linux.
Download, unpack, put `ronswanson` on your `PATH`, done. The `checksums.txt`
on each release is signed with keyless [cosign](https://docs.sigstore.dev/) if
you want to verify before running.

## With Go

```bash
go install github.com/tamnd/ronswanson-cli/cmd/ronswanson@latest
```

That puts `ronswanson` in `$(go env GOPATH)/bin`, which is `~/go/bin` unless
you moved it. Make sure that directory is on your `PATH`.

## From source

```bash
git clone https://github.com/tamnd/ronswanson-cli
cd ronswanson-cli
make build        # produces ./bin/ronswanson
./bin/ronswanson version
```

## Container image

```bash
docker run --rm ghcr.io/tamnd/ronswanson:latest --help
```

## Checking the install

```bash
ronswanson version
```

prints the version and exits.
