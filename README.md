# Masari

Copyright (c) 2017-2021 The Masari Project.
Copyright (c) 2014-2020 The Monero Project.
Portions Copyright (c) 2012-2013 The Cryptonote developers.

## Table of Contents

  - [Development resources](#development-resources)
  - [Vulnerability response](#vulnerability-response)
  - [Coverage](#coverage)
  - [Introduction](#introduction)
  - [About this project](#about-this-project)
  - [Supporting the project](#supporting-the-project)
  - [License](#license)
  - [Contributing](#contributing)
  - [Scheduled software upgrades](#scheduled-software-upgrades)
  - [Release staging schedule and protocol](#release-staging-schedule-and-protocol)
  - [Compiling Masari from source](#compiling-masari-from-source)
    - [Dependencies](#dependencies)
  - [Internationalization](#Internationalization)
  - [Using Tor](#using-tor)
  - [Pruning](#Pruning)
  - [Debugging](#Debugging)
  - [Known issues](#known-issues)

## Development resources

- Web: [getmasari.org](https://getmasari.org)
- Forum: [forum.getmasari.org](https://forum.getmasari.org)
- Mail: [dev@getmasari.org](mailto:dev@getmasari.org)
- GitHub: [https://github.com/masari-project/masari](https://github.com/masari-project/masari)
- IRC: [#masari on Freenode](https://webchat.freenode.net/?randomnick=1&channels=%23masari&prompt=1&uio=d4)

## Vulnerability response

- Our [Vulnerability Response Process](https://github.com/masari-project/meta/blob/master/VULNERABILITY_RESPONSE_PROCESS.md) encourages responsible disclosure

## Coverage

| Type      | Status |
|-----------|--------|
| License   | [![License](https://img.shields.io/badge/license-BSD3-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

## Introduction

Masari is a private, secure, untraceable, decentralised digital currency. You are your bank, you control your funds, and nobody can trace your transfers unless you allow them to do so.

**Privacy:** Masari uses a cryptographically sound system to allow you to send and receive funds without your transactions being easily revealed on the blockchain (the ledger of transactions that everyone has). This ensures that your purchases, receipts, and all transfers remain absolutely private by default.

**Security:** Using the power of a distributed peer-to-peer consensus network, every transaction on the network is cryptographically secured. Individual wallets have a 25-word mnemonic seed that is only displayed once and can be written down to backup the wallet. Wallet files are encrypted with a passphrase to ensure they are useless if stolen.

**Untraceability:** By taking advantage of ring signatures, a special property of a certain type of cryptography, Masari is able to ensure that transactions are not only untraceable but have an optional measure of ambiguity that ensures that transactions cannot easily be tied back to an individual user or computer.

**Scalability:** Masari aims to scale as a cryptocurrency to acheive high transaction speed and capacity while maintaining all of its privacy features as it explores unique solutions such as blocktree.

**Decentralization:** The utility of Masari depends on its decentralised peer-to-peer consensus network - anyone should be able to run the masari software, validate the integrity of the blockchain, and participate in all aspects of the masari network using consumer-grade commodity hardware. Decentralization of the masari network is maintained by software development that minimizes the costs of running the masari software and inhibits the proliferation of specialized, non-commodity hardware.  

## About this project

This is the core implementation of Masari, a scalability-focused fork of Monero. It is open source and completely free to use without restrictions, except for those specified in the license agreement below. There are no restrictions on anyone creating an alternative implementation of Masari that uses the protocol and network in a compatible manner.

As with many development projects, the repository on Github is considered to be the "staging" area for the latest changes. Before changes are merged into that branch on the main repository, they are tested by individual developers in their own branches, submitted as a pull request, and then subsequently tested by contributors who focus on testing and code reviews. That having been said, the repository should be carefully considered before using it in a production environment, unless there is a patch in the repository for a particular show-stopping issue you are experiencing. It is generally a better idea to use a tagged release for stability.

**Anyone is welcome to contribute to Masari's codebase!** If you have a fix or code change, feel free to submit it as a pull request directly to the "master" branch. In cases where the change is relatively small or does not affect other parts of the codebase it may be merged in immediately by any one of the collaborators. On the other hand, if the change is particularly large or complex, it is expected that it will be discussed at length either well in advance of the pull request being submitted, or even directly on the pull request.

## Supporting the project

Masari is a 100% community-sponsored endeavor. If you want to join our efforts, the easiest thing you can do is support the project financially.

The Masari donation address is: `5nYWvcvNThsLaMmrsfpRLBRou1RuGtLabUwYH7v6b88bem2J4aUwsoF33FbJuqMDgQjpDRTSpLCZu3dXpqXicE2uSWS4LUP` (viewkey: `99e21e00cce073c126e9aed800c9e2e82518534b3924b035a29436ff4f75bc0c`)

The Monero donation address is: `4A57eA3so6bEE8FUcaN1KtMXD3sxjjbvcKD3MF1pUgRi5PNHTpB7sYN2DmJv3EXxtZCWeG88tsVLzdfZJcmUFm52SbrfJWr` (viewkey: `c7a7c141581ac4436ba8bfb81dd67234720c565c696ef154a25c7e7314ce4b08`)

The Bitcoin donation address is: `1J1he4qtTuNpCxyEBozkeKfDpoeYxfE3rj`

There are a few mining pools that kindly donate a portion of their fees, [a list of them can be found on our Bitcointalk post](https://bitcointalk.org/index.php?topic=2159114.740). Others can be found on [MasariPools](http://masaripools.org/) and [CryptoIsMe](https://cryptoisme.com/coin/masari).

## License

See [LICENSE](LICENSE).

## Contributing

If you want to help out, see [CONTRIBUTING](CONTRIBUTING.md) for a set of guidelines.

## Scheduled software upgrades

Masari uses a fixed-schedule software upgrade (hard fork) mechanism to implement new features. This means that users of Masari (end users and service providers) should run current versions and upgrade their software on a regular schedule. Software upgrades occur during the months of April and October. The required software for these upgrades will be available prior to the scheduled date. Please check the repository prior to this date for the proper Masari software version. Below is the historical schedule and the projected schedule for the next upgrade.
Dates are provided in the format YYYY-MM-DD. 

| Fork Date         | Consensus version | Minimum Masari Version | Recommended Masari Version | Details                                                             |
| ----------------- | ----------------- | ---------------------- | -------------------------- | --------------------------------------------------------------------|
| 2017-10-05        | v2                | 0.1.2.0                | 0.1.2.0                    | Difficulty adjustment algorithm adjusted                            |
| 2017-11-29        | v3                | 0.1.3.0                | 0.1.3.1                    | Difficulty adjustment algorithm updated to WWHM                     |
| 2017-12-06        | v4                | 0.1.4.0                | 0.1.4.0                    | Difficulty adjustment tweaks                                        |
| 2018-05-01        | v5                | 0.2.0.0                | 0.2.0.2                    | Upstream track of v0.12.0 with Multisig, Subaddresses, CN variant 1 |
| 2018-05-05        | v6                | 0.2.3.0                | 0.2.3.0                    | LWMA + stricter FTL settings                                        |
| 2018-06-18        | v7                | 0.2.4.0                | 0.2.4.5                    | CryptoNight-Fast PoW                                                |
| 2019-01-26        | v8                | 0.3.0.0                | 0.3.0.0                    | SECOR (uncle mining) protocol, multi-output Bulletproofs, CNFastv2  |
| TBD               |                   | 0.4.0.0                | 0.4.0.0                    | Rebase with Monero v0.17                                            |
X's indicate that these details have not been determined as of commit date.

## Release staging schedule and protocol

Approximately three months prior to a scheduled software upgrade, a branch from Master will be created with the new release version tag. Pull requests that address bugs should then be made to both Master and the new release branch. Pull requests that require extensive review and testing (generally, optimizations and new features) should *not* be made to the release branch. 

## Compiling Masari from source

### Dependencies

The following table summarizes the tools and libraries required to build. A
few of the libraries are also included in this repository (marked as
"Vendored"). By default, the build uses the library installed on the system
and ignores the vendored sources. However, if no library is found installed on
the system, then the vendored source will be built and used. The vendored
sources are also used for statically-linked builds because distribution
packages often include only shared library binaries (`.so`) but not static
library archives (`.a`).

| Dep          | Min. version  | Vendored | Debian/Ubuntu pkg    | Arch pkg     | Void pkg           | Fedora pkg          | Optional | Purpose         |
| ------------ | ------------- | -------- | -------------------- | ------------ | ------------------ | ------------------- | -------- | --------------- |
| GCC          | 4.7.3         | NO       | `build-essential`    | `base-devel` | `base-devel`       | `gcc`               | NO       |                 |
| CMake        | 3.5           | NO       | `cmake`              | `cmake`      | `cmake`            | `cmake`             | NO       |                 |
| pkg-config   | any           | NO       | `pkg-config`         | `base-devel` | `base-devel`       | `pkgconf`           | NO       |                 |
| Boost        | 1.58          | NO       | `libboost-all-dev`   | `boost`      | `boost-devel`      | `boost-devel`       | NO       | C++ libraries   |
| OpenSSL      | basically any | NO       | `libssl-dev`         | `openssl`    | `libressl-devel`   | `openssl-devel`     | NO       | sha256 sum      |
| libzmq       | 3.0.0         | NO       | `libzmq3-dev`        | `zeromq`     | `zeromq-devel`     | `zeromq-devel`      | NO       | ZeroMQ library  |
| OpenPGM      | ?             | NO       | `libpgm-dev`         | `libpgm`     |                    | `openpgm-devel`     | NO       | For ZeroMQ      |
| libnorm[2]   | ?             | NO       | `libnorm-dev`        |              |                    |                     | YES      | For ZeroMQ      |
| libunbound   | 1.4.16        | YES      | `libunbound-dev`     | `unbound`    | `unbound-devel`    | `unbound-devel`     | NO       | DNS resolver    |
| libsodium    | ?             | NO       | `libsodium-dev`      | `libsodium`  | `libsodium-devel`  | `libsodium-devel`   | NO       | cryptography    |
| libunwind    | any           | NO       | `libunwind8-dev`     | `libunwind`  | `libunwind-devel`  | `libunwind-devel`   | YES      | Stack traces    |
| liblzma      | any           | NO       | `liblzma-dev`        | `xz`         | `liblzma-devel`    | `xz-devel`          | YES      | For libunwind   |
| libreadline  | 6.3.0         | NO       | `libreadline6-dev`   | `readline`   | `readline-devel`   | `readline-devel`    | YES      | Input editing   |
| ldns         | 1.6.17        | NO       | `libldns-dev`        | `ldns`       | `libldns-devel`    | `ldns-devel`        | YES      | SSL toolkit     |
| expat        | 1.1           | NO       | `libexpat1-dev`      | `expat`      | `expat-devel`      | `expat-devel`       | YES      | XML parsing     |
| GTest        | 1.5           | YES      | `libgtest-dev`[1]    | `gtest`      | `gtest-devel`      | `gtest-devel`       | YES      | Test suite      |
| Doxygen      | any           | NO       | `doxygen`            | `doxygen`    | `doxygen`          | `doxygen`           | YES      | Documentation   |
| Graphviz     | any           | NO       | `graphviz`           | `graphviz`   | `graphviz`         | `graphviz`          | YES      | Documentation   |
| lrelease     | ?             | NO       | `qttools5-dev-tools` | `qt5-tools`  | `qt5-tools`        | `qt5-linguist`      | YES      | Translations    |
| libhidapi    | ?             | NO       | `libhidapi-dev`      | `hidapi`     | `hidapi-devel`     | `hidapi-devel`      | YES      | Hardware wallet |
| libusb       | ?             | NO       | `libusb-1.0-0-dev`   | `libusb`     | `libusb-devel`     | `libusbx-devel`     | YES      | Hardware wallet |
| libprotobuf  | ?             | NO       | `libprotobuf-dev`    | `protobuf`   | `protobuf-devel`   | `protobuf-devel`    | YES      | Hardware wallet |
| protoc       | ?             | NO       | `protobuf-compiler`  | `protobuf`   | `protobuf`         | `protobuf-compiler` | YES      | Hardware wallet |
| libudev      | ?             | No       | `libudev-dev`        | `systemd`    | `eudev-libudev-devel` | `systemd-devel`     | YES      | Hardware wallet |

[1] On Debian/Ubuntu `libgtest-dev` only includes sources and headers. You must
build the library binary manually. This can be done with the following command ```sudo apt-get install libgtest-dev && cd /usr/src/gtest && sudo cmake . && sudo make && sudo mv libg* /usr/lib/ ```
[2] libnorm-dev is needed if your zmq library was built with libnorm, and not needed otherwise

Install all dependencies at once on Debian/Ubuntu:

``` sudo apt update && sudo apt install build-essential cmake pkg-config libboost-all-dev libssl-dev libzmq3-dev libunbound-dev libsodium-dev libunwind8-dev liblzma-dev libreadline6-dev libldns-dev libexpat1-dev doxygen graphviz libpgm-dev qttools5-dev-tools libhidapi-dev libusb-1.0-0-dev libprotobuf-dev protobuf-compiler libudev-dev```

Install all dependencies at once on macOS with the provided Brewfile:
``` brew update && brew bundle --file=contrib/brew/Brewfile ```

FreeBSD 12.1 one-liner required to build dependencies:
```pkg install git gmake cmake pkgconf boost-libs libzmq4 libsodium```

### Cloning the repository

Clone recursively to pull-in needed submodule(s):

`$ git clone --recursive https://github.com/masari-project/masari`

If you already have a repo cloned, initialize and update:

`$ cd masari && git submodule init && git submodule update`

### Build instructions

Masari uses the CMake build system and a top-level [Makefile](Makefile) that
invokes cmake commands as needed.

#### On Linux and macOS

* Install the dependencies
* Change to the root of the source code directory, change to the most recent release branch, and build:

    cd masari
    make

    *Optional*: If your machine has several cores and enough memory, enable
    parallel build by running `make -j<number of threads>` instead of `make`. For
    this to be worthwhile, the machine should have one core and about 2GB of RAM
    available per thread.

* The resulting executables can be found in `build/release/bin`

* Add `PATH="$PATH:$HOME/masari/build/release/bin"` to `.profile`

* Run Masari with `masarid --detach`

* **Optional**: build and run the test suite to verify the binaries:

        make release-test

    *NOTE*: `core_tests` test may take a few hours to complete.

* **Optional**: to build binaries suitable for debugging:

         make debug

* **Optional**: to build statically-linked binaries:

         make release-static

* **Optional**: build documentation in `doc/html` (omit `HAVE_DOT=YES` if `graphviz` is not installed):

        HAVE_DOT=YES doxygen Doxyfile

#### On Windows:

Binaries for Windows are built on Windows using the MinGW toolchain within
[MSYS2 environment](https://www.msys2.org). The MSYS2 environment emulates a
POSIX system. The toolchain runs within the environment and *cross-compiles*
binaries that can run outside of the environment as a regular Windows
application.

**Preparing the build environment**

* Download and install the [MSYS2 installer](https://www.msys2.org), either the 64-bit or the 32-bit package, depending on your system.
* Open the MSYS shell via the `MSYS2 Shell` shortcut
* Update packages using pacman:  

    ```bash
    pacman -Syu
    ```

* Exit the MSYS shell using Alt+F4  
* Edit the properties for the `MSYS2 Shell` shortcut changing "msys2_shell.bat" to "msys2_shell.cmd -mingw64" for 64-bit builds or "msys2_shell.cmd -mingw32" for 32-bit builds
* Restart MSYS shell via modified shortcut and update packages again using pacman:  

    ```bash
    pacman -Syu
    ```


* Install dependencies:

    To build for 64-bit Windows:

    ```bash
    pacman -S mingw-w64-x86_64-toolchain make mingw-w64-x86_64-cmake mingw-w64-x86_64-boost mingw-w64-x86_64-openssl mingw-w64-x86_64-zeromq mingw-w64-x86_64-libsodium mingw-w64-x86_64-hidapi
    ```

    To build for 32-bit Windows:

    ```bash
    pacman -S mingw-w64-i686-toolchain make mingw-w64-i686-cmake mingw-w64-i686-boost mingw-w64-i686-openssl mingw-w64-i686-zeromq mingw-w64-i686-libsodium mingw-w64-i686-hidapi
    ```

* Open the MingW shell via `MinGW-w64-Win64 Shell` shortcut on 64-bit Windows
  or `MinGW-w64-Win64 Shell` shortcut on 32-bit Windows. Note that if you are
  running 64-bit Windows, you will have both 64-bit and 32-bit MinGW shells.

**Cloning**

* To git clone, run:

    ```bash
    git clone --recursive https://github.com/masari-project/masari.git
    ```

**Building**

* Change to the cloned directory, run:

    ```bash
    cd masari
    ```

* If you would like a specific [version/tag](https://github.com/masari-project/masari/tags), do a git checkout for that version. eg. 'v0.4.0.0'. If you don't care about the version and just want binaries from master, skip this step:

    ```bash
    git checkout v0.4.0.0
    ```

* If you are on a 64-bit system, run:

    ```bash
    make release-static-win64
    ```

* If you are on a 32-bit system, run:

    ```bash
    make release-static-win32
    ```

* The resulting executables can be found in `build/release/bin`

* **Optional**: to build Windows binaries suitable for debugging on a 64-bit system, run:

    ```bash
    make debug-static-win64
    ```

* **Optional**: to build Windows binaries suitable for debugging on a 32-bit system, run:

    ```bash
    make debug-static-win32
    ```

* The resulting executables can be found in `build/debug/bin`

### On FreeBSD:

The project can be built from scratch by following instructions for Linux above(but use `gmake` instead of `make`). 
If you are running Masari in a jail, you need to add `sysvsem="new"` to your jail configuration, otherwise lmdb will throw the error message: `Failed to open lmdb environment: Function not implemented`.

### On OpenBSD:

You will need to add a few packages to your system. `pkg_add cmake gmake zeromq libiconv boost`.

The `doxygen` and `graphviz` packages are optional and require the xbase set.
Running the test suite also requires `py-requests` package.

Build masari: `env DEVELOPER_LOCAL_TOOLS=1 BOOST_ROOT=/usr/local gmake release-static`

Note: you may encounter the following error when compiling the latest version of Masari as a normal user:

```
LLVM ERROR: out of memory
c++: error: unable to execute command: Abort trap (core dumped)
```

Then you need to increase the data ulimit size to 2GB and try again: `ulimit -d 2000000`

### On NetBSD:

Check that the dependencies are present: `pkg_info -c libexecinfo boost-headers boost-libs protobuf readline libusb1 zeromq git-base pkgconf gmake cmake | more`, and install any that are reported missing, using `pkg_add` or from your pkgsrc tree.  Readline is optional but worth having.

Third-party dependencies are usually under `/usr/pkg/`, but if you have a custom setup, adjust the "/usr/pkg" (below) accordingly.

Clone the masari repository recursively and checkout the most recent release as described above. Then build masari: `gmake BOOST_ROOT=/usr/pkg LDFLAGS="-Wl,-R/usr/pkg/lib" release`.  The resulting executables can be found in `build/NetBSD/[Release version]/Release/bin/`.

### On Solaris:

The default Solaris linker can't be used, you have to install GNU ld, then run cmake manually with the path to your copy of GNU ld:

```bash
mkdir -p build/release
cd build/release
cmake -DCMAKE_LINKER=/path/to/ld -D CMAKE_BUILD_TYPE=Release ../..
cd ../..
```

Then you can run make as usual.

### On Linux for Android (using docker):

```bash
# Build image (for ARM 32-bit)
docker build -f utils/build_scripts/android32.Dockerfile -t masari-android .
# Build image (for ARM 64-bit)
docker build -f utils/build_scripts/android64.Dockerfile -t masari-android .
# Create container
docker create -it --name masari-android masari-android bash
# Get binaries
docker cp masari-android:/src/build/release/bin .
```

### Building portable statically linked binaries

By default, in either dynamically or statically linked builds, binaries target the specific host processor on which the build happens and are not portable to other processors. Portable binaries can be built using the following targets:

* ```make release-static-linux-x86_64``` builds binaries on Linux on x86_64 portable across POSIX systems on x86_64 processors
* ```make release-static-linux-i686``` builds binaries on Linux on x86_64 or i686 portable across POSIX systems on i686 processors
* ```make release-static-linux-armv8``` builds binaries on Linux portable across POSIX systems on armv8 processors
* ```make release-static-linux-armv7``` builds binaries on Linux portable across POSIX systems on armv7 processors
* ```make release-static-linux-armv6``` builds binaries on Linux portable across POSIX systems on armv6 processors
* ```make release-static-win64``` builds binaries on 64-bit Windows portable across 64-bit Windows systems
* ```make release-static-win32``` builds binaries on 64-bit or 32-bit Windows portable across 32-bit Windows systems

### Cross Compiling

You can also cross-compile static binaries on Linux for Windows and macOS with the `depends` system.

* ```make depends target=x86_64-linux-gnu``` for 64-bit linux binaries.
* ```make depends target=x86_64-w64-mingw32``` for 64-bit windows binaries.
  * Requires: `python3 g++-mingw-w64-x86-64 wine1.6 bc`
* ```make depends target=x86_64-apple-darwin11``` for macOS binaries.
  * Requires: `cmake imagemagick libcap-dev librsvg2-bin libz-dev libbz2-dev libtiff-tools python-dev`
* ```make depends target=i686-linux-gnu``` for 32-bit linux binaries.
  * Requires: `g++-multilib bc`
* ```make depends target=i686-w64-mingw32``` for 32-bit windows binaries.
  * Requires: `python3 g++-mingw-w64-i686`
* ```make depends target=arm-linux-gnueabihf``` for armv7 binaries.
  * Requires: `g++-arm-linux-gnueabihf`
* ```make depends target=aarch64-linux-gnu``` for armv8 binaries.
  * Requires: `g++-aarch64-linux-gnu`
* ```make depends target=riscv64-linux-gnu``` for RISC V 64 bit binaries.
  * Requires: `g++-riscv64-linux-gnu`
* ```make depends target=x86_64-unknown-freebsd``` for freebsd binaries.
  * Requires: `clang-8`
* ```make depends target=arm-linux-android``` for 32bit android binaries
* ```make depends target=aarch64-linux-android``` for 64bit android binaries


The required packages are the names for each toolchain on apt. Depending on your distro, they may have different names.

Using `depends` might also be easier to compile Masari on Windows than using MSYS. Activate Windows Subsystem for Linux (WSL) with a distro (for example Ubuntu), install the apt build-essentials and follow the `depends` steps as depicted above.

The produced binaries still link libc dynamically. If the binary is compiled on a current distribution, it might not run on an older distribution with an older installation of libc. Passing `-DBACKCOMPAT=ON` to cmake will make sure that the binary will run on systems having at least libc version 2.17.


## Running masarid

The build places the binary in `bin/` sub-directory within the build directory
from which cmake was invoked (repository root by default). To run in the
foreground:

```bash
./bin/masarid
```

To list all available options, run `./bin/masarid --help`.  Options can be
specified either on the command line or in a configuration file passed by the
`--config-file` argument.  To specify an option in the configuration file, add
a line with the syntax `argumentname=value`, where `argumentname` is the name
of the argument without the leading dashes, for example, `log-level=1`.

To run in background:

```bash
./bin/masarid --log-file masarid.log --detach
```

To run as a systemd service, copy
[masarid.service](utils/systemd/masarid.service) to `/etc/systemd/system/` and
[masarid.conf](utils/conf/masarid.conf) to `/etc/`. The [example
service](utils/systemd/masarid.service) assumes that the user `masari` exists
and its home is the data directory specified in the [example
config](utils/conf/masarid.conf).

If you're on Mac, you may need to add the `--max-concurrency 1` option to
masari-wallet-cli, and possibly masarid, if you get crashes refreshing.

## Internationalization

See [README.i18n.md](README.i18n.md).

## Using Tor

> There is a new, still experimental, [integration with Tor](ANONYMITY_NETWORKS.md). The
> feature allows connecting over IPv4 and Tor simultaneously - IPv4 is used for
> relaying blocks and relaying transactions received by peers whereas Tor is
> used solely for relaying transactions received over local RPC. This provides
> privacy and better protection against surrounding node (sybil) attacks.

While Masari isn't made to integrate with Tor, it can be used wrapped with torsocks, by
setting the following configuration parameters and environment variables:

* `--p2p-bind-ip 127.0.0.1` on the command line or `p2p-bind-ip=127.0.0.1` in
  masarid.conf to disable listening for connections on external interfaces.
* `--no-igd` on the command line or `no-igd=1` in masarid.conf to disable IGD
  (UPnP port forwarding negotiation), which is pointless with Tor.
* `DNS_PUBLIC=tcp` or `DNS_PUBLIC=tcp://x.x.x.x` where x.x.x.x is the IP of the
  desired DNS server, for DNS requests to go over TCP, so that they are routed
  through Tor. When IP is not specified, masarid uses the default list of
  servers defined in [src/common/dns_utils.cpp](src/common/dns_utils.cpp).
* `TORSOCKS_ALLOW_INBOUND=1` to tell torsocks to allow masarid to bind to interfaces
   to accept connections from the wallet. On some Linux systems, torsocks
   allows binding to localhost by default, so setting this variable is only
   necessary to allow binding to local LAN/VPN interfaces to allow wallets to
   connect from remote hosts. On other systems, it may be needed for local wallets
   as well.
* Do NOT pass `--detach` when running through torsocks with systemd, (see
  [utils/systemd/masarid.service](utils/systemd/masarid.service) for details).
* If you use the wallet with a Tor daemon via the loopback IP (eg, 127.0.0.1:9050),
  then use `--untrusted-daemon` unless it is your own hidden service.

Example command line to start masarid through Tor:

```bash
DNS_PUBLIC=tcp torsocks masarid --p2p-bind-ip 127.0.0.1 --no-igd
```

### Using Tor on Tails

TAILS ships with a very restrictive set of firewall rules. Therefore, you need
to add a rule to allow this connection too, in addition to telling torsocks to
allow inbound connections. Full example:

```bash
sudo iptables -I OUTPUT 2 -p tcp -d 127.0.0.1 -m tcp --dport 18081 -j ACCEPT
DNS_PUBLIC=tcp torsocks ./masarid --p2p-bind-ip 127.0.0.1 --no-igd --rpc-bind-ip 127.0.0.1 \
    --data-dir /home/amnesia/Persistent/your/directory/to/the/blockchain
```

## Pruning

One can store a pruned blockchain, to use less storage.
A pruned blockchain can only serve part of the historical chain data to other peers, but is otherwise identical in
functionality to the full blockchain.
To use a pruned blockchain, it is best to start the initial sync with --prune-blockchain. However, it is also possible
to prune an existing blockchain using the masari-blockchain-prune tool or using the --prune-blockchain masarid option
with an existing chain. If an existing chain exists, pruning will temporarily require disk space to store both the full
and pruned blockchains.

## Debugging

This section contains general instructions for debugging failed installs or problems encountered with Masari. First ensure you are running the latest version built from the Github repo.

### Obtaining stack traces and core dumps on Unix systems

We generally use the tool `gdb` (GNU debugger) to provide stack trace functionality, and `ulimit` to provide core dumps in builds which crash or segfault.

* To use `gdb` in order to obtain a stack trace for a build that has stalled:

Run the build.

Once it stalls, enter the following command:

```bash
gdb /path/to/masarid `pidof masarid`
```

Type `thread apply all bt` within gdb in order to obtain the stack trace

* If however the core dumps or segfaults:

Enter `ulimit -c unlimited` on the command line to enable unlimited filesizes for core dumps

Enter `echo core | sudo tee /proc/sys/kernel/core_pattern` to stop cores from being hijacked by other tools

Run the build.

When it terminates with an output along the lines of "Segmentation fault (core dumped)", there should be a core dump file in the same directory as masarid. It may be named just `core`, or `core.xxxx` with numbers appended.

You can now analyse this core dump with `gdb` as follows:

```bash
gdb /path/to/masarid /path/to/dumpfile
```

Print the stack trace with `bt`

 * If a program crashed and cores are managed by systemd, the following can also get a stack trace for that crash:

```bash
coredumpctl -1 gdb
```

#### To run Masari within gdb:

Type `gdb /path/to/masarid`

Pass command-line options with `--args` followed by the relevant arguments

Type `run` to run masarid

### Analysing memory corruption

There are two tools available:

#### ASAN

Configure Masari with the -D SANITIZE=ON cmake flag, eg:

```bash
cd build/debug && cmake -D SANITIZE=ON -D CMAKE_BUILD_TYPE=Debug ../..
```

You can then run the masari tools normally. Performance will typically halve.

#### valgrind

Install valgrind and run as `valgrind /path/to/masarid`. It will be slow.

### LMDB

Instructions for debugging suspected blockchain corruption as per @HYC

There is an `mdb_stat` command in the LMDB source that can print statistics about the database but it's not routinely built. This can be built with the following command:

```bash
cd ~/masari/external/db_drivers/liblmdb && make
```

The output of `mdb_stat -ea <path to blockchain dir>` will indicate inconsistencies in the blocks, block_heights and block_info table.

The output of `mdb_dump -s blocks <path to blockchain dir>` and `mdb_dump -s block_info <path to blockchain dir>` is useful for indicating whether blocks and block_info contain the same keys.

These records are dumped as hex data, where the first line is the key and the second line is the data.

# Known Issues

## Protocols

### Socket-based

Because of the nature of the socket-based protocols that drive masari, certain protocol weaknesses are somewhat unavoidable at this time. While these weaknesses can theoretically be fully mitigated, the effort required (the means) may not justify the ends. As such, please consider taking the following precautions if you are a masari node operator:

- Run `masarid` on a "secured" machine. If operational security is not your forte, at a very minimum, have a dedicated a computer running `masarid` and **do not** browse the web, use email clients, or use any other potentially harmful apps on your `masarid` machine. **Do not click links or load URL/MUA content on the same machine**. Doing so may potentially exploit weaknesses in commands which accept "localhost" and "127.0.0.1".
- If you plan on hosting a public "remote" node, start `masarid` with `--restricted-rpc`. This is a must.

### Blockchain-based

Certain blockchain "features" can be considered "bugs" if misused correctly. Consequently, please consider the following:

- When receiving masari, be aware that it may be locked for an arbitrary time if the sender elected to, preventing you from spending that masari until the lock time expires. You may want to hold off acting upon such a transaction until the unlock time lapses. To get a sense of that time, you can consider the remaining blocktime until unlock as seen in the `show_transfers` command.
