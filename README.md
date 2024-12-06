# OpenSSL Binaries Flutter Plugin

This repository contains a Flutter plugin that provides pre-compiled OpenSSL
binaries (libcrypto and libssl) that have been compiled from the source files
for [version 3.3.2](https://github.com/openssl/openssl/tree/openssl-3.3.2).
Currently, only Android is supported.

## Usage

Since this plugin is currently not available on pub.dev, you can add it to your
Flutter project as a git dependency using the following command:

```sh
flutter pub add flutter_openssl_binaries --git-url=https://github.com/JKRhb/flutter_openssl_binaries
```

## License

As OpenSSL is licensed under the Apache 2.0 license, the content in this
repository is available under the same license.
See the `LICENSE` file for more information.

    SPDX-License-Identifier: Apache-2.0
