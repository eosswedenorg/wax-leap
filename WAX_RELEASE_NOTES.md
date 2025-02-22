# WAX Release Notes

## General

WAX software version 2.0 is a port of WAX-specific patches to EOSIO
2.0 software by Block.One.

The upgrade procedure from WAX 1.8.4 to 2.0 is similar to upgrading
EOSIO from 1.8 to 2.0. The release notes of EOSIO apply to WAX
software as well. All WASM virtual machine options available in EOSIO
are also supported in WAX, and recommendations on their use are the
same as for respective releases of EOSIO software.

Unlike 1.8, the server version string is controlled by
`CMakeLists.txt` and is no longer derived from Git tags.

In order to keep most compatibility with upstream software, the
proposed versioning schema will add `waxNN` to VERSION_PATCH in
`CMakeLists.txt`.


## Release `v2.0.5wax01`

EOSIO 2.0.4 was merged with WAX 1.8.4, with necessary
modifications. Later on, EOSIO 2.0.5 was merged in.


The following files were taken from vanilla EOSIO without
modifications, because WAX changes were not necessary:

```
libraries/testing/include/eosio/testing/tester.hpp
libraries/testing/tester.cpp
```

`scripts/eosio_build.sh`: `-r` option in wax-1.8.4 is setting
PUBLIC_ROOT_KEY, but it's not used in release binaries. Skipping in
wax-2.0.


`unittests/eosio_system_tester.hpp` line 415: set buyram sum to "0.5
WAX".

Testing scripts were adjusted and bugfixed, so that full automated
testing can succeed on WAX.


## Release `v2.0.9wax01`

EOSIO 2.0.9 merged

## Release `v2.0.10wax01`

EOSIO 2.0.10 merged

## Release `v2.0.11wax01`

EOSIO 2.0.11 merged

## Release `v2.0.12wax01`

EOSIO 2.0.12 merged

## Release `v2.0.13wax01`

EOSIO 2.0.13 merged

## Release candidate `v3.1.0wax01-rc3`

EOS Network Foundation has taken over the EOSIO development from Block
One, and the first new release will be called Mandel 3.1.0. This tag
is a merge of WAX-specific intrinsic into the Mandel code.

Mandel repository: https://github.com/eosnetworkfoundation/mandel

WAX-Mandel repository: https://github.com/cc32d9/wax-mandel

## Release candidate `v3.1.0wax01-rc4`

The EOSIO development is now called Antelope, and the nodeos 
implememtation is called Leap. Apart from naming, the new RC contains a few 
fixes.

Leap repository: https://github.com/AntelopeIO/leap

WAX-Leap repository: https://github.com/cc32d9/wax-leap

## Release `v3.1.0wax01`

Snapshot unit tests are not ported to WAX properly and need to be re-done.

## Release `v3.1.0wax02pr124`

Merging https://github.com/AntelopeIO/leap/pull/124
[3.1] Allow for larger subjective CPU billing amounts

## Release `v3.1.1wax01`

Merged with Leap 3.1.1

## Release `v3.1.2wax01`

Merged with Leap 3.1.2

## Release `v3.1.3wax01`

Merged with Leap 3.1.3

## Release `v3.1.4wax01`

Merged with Leap 3.1.4

## Release `v3.1.4wax02`

bugfix in version string

