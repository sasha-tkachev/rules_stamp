# Stamp rules for Bazel

## Setup

```py
http_archive(
    name = "rules_stamp",
    url = "https://github.com/sasha-tkachev/rules_stamp/archive/6cf5018cd384afe4bd43f4a0eeb414af03451115.tar.gz",
    strip_prefix = "rules_stamp-6cf5018cd384afe4bd43f4a0eeb414af03451115.tar.gz",
    sha256 = "357ae4ba73e465f692c5de911581c8981f30d6eecf5278f40b3f800ca12e6706",
)
```
## Rules

### stamp

Extracts the stamp values out based on the specified keys and outputs them into a file for format `STAMP_<key>`. So one can depend on it in another rule or binary and get the stamping value easier, e.g. by just using `cat`.

`stamp(name, stamp_keys)`
