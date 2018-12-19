Change log for eprints2bags
===========================

(Next release &ndash; TBD)
-------------

* Fix handling lack of `official_url` elements in EPrints records

Version 1.4.0
-------------

* Fix an important network handling bug that could cause incomplete records to be saved
* Fix bugs in handling network exceptions while downloading content from servers
* Improve detection of file system limitations
* Makes `-o` an optional argument
* Fix a missing Python package import
* Rename `CONDUCT.md` to [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) so that GitHub can find it
* Add [`CONTRIBUTING.md`](CONTRIBUTING.md),
* Update the documentation
* Fix some other minor bugs
* Minor internal code refactoring


Version 1.3.0
-------------

Eprints2bags now generates uncompressed [ZIP](https://www.loc.gov/preservation/digital/formats/fdd/fdd000354.shtml) archives of bags by default, instead of using compressed [tar](https://en.wikipedia.org/wiki/Tar_(computing)) format.  This was done in the belief that ZIP format is more widely supported and because compressed archive file contents may be more difficult to recover if the archive file becomes corrupted.  Also, the program `eprints2bags` now uses the run-time environment's keychain/keyring services to store the user name and password between runs, for convenience when running the program repeatedly.  Finally, some of the the command-line options have been changed.