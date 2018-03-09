# OracleDriver

OracleDriver is a pure Swift database driver for Oracle databases.
Supported platforms: macOS and Linux

# Required Software

## Oracle Instant Client 

Download binary package from [here](http://www.oracle.com/technetwork/database/database-technologies/instant-client/overview/index.html). Oracle account is required.

## Oracle ODPI-C package

### macOS

Install via Homebrew

```sh
brew install odpi
```

### Linux

TBD

# Usage

Add this repository to your project as a dependency:

```swift
/* ... */
let package = Package(
    /* ... */
    dependencies: [
        /* ... */
        .package(url: "https://github.com/segabor/OracleDriver", .branch("master"))
        /* ... */
    ],
    /* ... */
)
```

Make sure system library path includes location of Oracle client driver. OracleDriver will want to look for Oracle client library via DYLD_LIBRARY_PATH / LD_LIBRARY_PATH.

Details are in [ODPI-C Installation doc](https://oracle.github.io/odpi/doc/installation.html)
