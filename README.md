# SwiftShader-ex

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Build Status](https://travis-ci.org/google/swiftshader.svg?branch=master)](https://travis-ci.org/google/swiftshader) [![Build status](https://ci.appveyor.com/api/projects/status/yrmyvb34j22jg1uj?svg=true)](https://ci.appveyor.com/project/c0d1f1ed/swiftshader)

SwiftShader is a high-performance CPU-based implementation of the OpenGL ES and Direct3D 9 graphics APIs<sup>1</sup><sup>2</sup>. Its goal is to provide hardware independence for advanced 3D graphics.

Usage
-----

The SwiftShader libraries act as drop-in replacements for graphics drivers.

On Windows, most applications can be made to use SwiftShader's DLLs by placing them in the same folder as the executable. On Linux, the LD\_LIBRARY\_PATH environment variable or -rpath linker option can be used to direct applications to search for shared libraries in the indicated directory first.

Prebuilt binaries can be found in the releases section at https://github.com/ddrmax/swiftshader-ex/releases

Third-Party Dependencies
------------------------

The [third_party](third_party/) directory contains projects which originated outside of SwiftShader:

[LLVM](third_party/LLVM/) contains an outdated and diverged copy of the [LLVM](http://llvm.org/) compiler framework. Until further notice, maintenance fixes can be made directly in the SwiftShader repository.

[subzero](third_party/subzero/) contains a fork of the [Subzero](https://chromium.googlesource.com/native_client/pnacl-subzero/) project. It is part of Google Chrome's (Portable) [Native Client](https://developer.chrome.com/native-client) project. Its authoritative source is at [https://chromium.googlesource.com/native_client/pnacl-subzero/](https://chromium.googlesource.com/native_client/pnacl-subzero/). The fork was made using [git-subtree](https://github.com/git/git/blob/master/contrib/subtree/git-subtree.txt) to include all of Subzero's history, and until further notice it should **not** diverge from the upstream project. Contributions must be tested using the [README](third_party/subzero/docs/README.rst) instructions, reviewed at [https://chromium-review.googlesource.com](https://chromium-review.googlesource.com/q/project:native_client%252Fpnacl-subzero), and then pulled into the SwiftShader repository.

[llvm-subzero](third_party/llvm-subzero/) contains a minimized set of LLVM dependencies of the Subzero project.

[PowerVR_SDK](third_party/PowerVR_SDK/) contains a subset of the [PowerVR Graphics Native SDK](https://github.com/powervr-graphics/Native_SDK) for running several sample applications.

[googletest](third_party/googletest/) contains the [Google Test](https://github.com/google/googletest) project, as a Git submodule. It is used for running unit tests for Chromium, and Reactor unit tests. Run `git submodule update --init` to obtain/update the code. Any contributions should be made upstream.

Documentation
-------------

See [docs/Index.md](docs/Index.md).

License
-------

The SwiftShader project and "SwiftShader EX" are licensed under the Apache License Version 2.0. You can find a copy of it in [LICENSE.txt](LICENSE.txt).

Files in the third_party folder are subject to their respective license.

Authors and Contributors
------------------------

The legal authors for copyright purposes are listed in [AUTHORS.txt](AUTHORS.txt).

[CONTRIBUTORS.txt](CONTRIBUTORS.txt) contains a list of names of individuals who have contributed to SwiftShader. If you're not on the list, but you've signed the [Google CLA](https://cla.developers.google.com/clas) and have contributed more than a formatting change, feel free to request to be added.

Disclaimer
----------

1. Trademarks are the property of their respective owners.
2. We do not claim official conformance with any graphics APIs at this moment.
3. This is not an official Google product.
4. There is no guarantee that the "SwiftShader EX" are going to be proposed to the official Google SwiftShader repository
