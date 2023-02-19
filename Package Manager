Since this software ecosystem is attempting to be another a write-once, run-anywhere (WORA) system, it's important to address several things head-on. Firstly, in terms of
package management, which should attempt to handle both the case of packaging a library for reuse, and packaging an artifact for distribution. Hence, it's intended that
the package manager may not be unique to this system, but that the bare-minimum package manager provide the following.

# Package Management
There are several package managers that provide code via source, and others that provide code that is already compiled and packaged. It's preferred that the package be
made available without requiring the user to download a source code compiler and linker to use. It's intended that the package be distributed in an intermediary language
(IL) and that the packaging software either provide it as-is (for JIT compilation) or compile it to a target (for AOT compilation) during download and installation.

It's possible to have the package manager use extensions to cross-compile and cross-link for embedded applications, and as such, it's not naturally assumed that the
package manager be running on the target.

## Embedded Firmware Applications
Firmware may be deployed in a memory-poor environment and variations on the package manager may account for this in the linking process. It may also choose to require or
ignore certain validations before incorporating a package into the application. Finally, it's assumed that any embedded application may entirely use AOT compiling and 
trim excessively using the information available for what will and will not be necessary for the final application, including whether or not there are needs to address
reentry of library functions. Likewise, a package employed as firmware will likely have erased the manifest information and signatures. For embedded applications running
on an operating system, this may or may not also be the case.

## Package Validation
In addition to packaging for distribution, the package manager should also permit signing of both reusable and installable packages. Multiple signatures should be allowed,
and a distributor can filter out packages based on signatures. 

It's intended that the primary signature be created by the compiler itself (via the compiler designer) and
this is used to show that the proofs and types have been fully checked, and it also gives a manifest of the additional knowledge inferred about the types, such as inferred
linearity, directionality, etc. This proof-manifest may also be used by database systems, web, etc. to validate the entire package before permitting it to be used, or even
just to validate and allow subsets of types and functions.

The secondary signature may be provided by the development company, used to sign the package as being the intended package sourced from them. This is used as an 
authentication mechanism, ensuring that the package has not been modified. It may be necessary to have the user of the package manager software to accept a certificate
from the developer before deploying or using the package.

Tertiary external signatures may be imposed by distributors, such as a mobile store, an operating system manufacturer, a government, or even an IT organization, for the 
purposes of evaluating the software for particular requirements. Such uses may include:
* Conformance to Static Analysis evaluation for an organization
* Conformance to Export Compliance
* Conformance to Acceptance Testing for a store

## Drivers
In addition to static analysis for conformance, the primary manifest may also include information for how a driver is to be used by the system. For instance, it will
record interrupts used/overridden, and DMA locations used.
