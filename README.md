# Uptake demo: HAP-Java

This is [HAP-Java](https://github.com/hap-java/HAP-Java) (MIT, see `LICENSE`) at the commit just before its
BouncyCastle upgrade, used to show [Uptake](https://github.com/usv240/uptake) working on a live repository.

Dependabot is enabled for `org.bouncycastle`. Upgrading `bcprov-jdk15on` removes 13 known advisories and breaks
compilation, because BouncyCastle deleted the `org.bouncycastle.crypto.tls` package the code uses.

When Dependabot opens that PR, the `Uptake` workflow runs IBM Bob in Uptake's locked mode, proves the repair
offline, commits it to the PR and comments the receipt. See the pull requests tab.

The original project README is in `README.upstream.md`.
