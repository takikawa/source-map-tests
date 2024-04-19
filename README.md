WIP repo for source map test proof of concept
---------------------------------------------

How to run in Firefox:
  * Check out mozilla-unified (see [Firefox dev setup](https://firefox-source-docs.mozilla.org/setup/index.html) under "Setting up your machine" for details, note that you can use git via [git-cinnabar](https://github.com/glandium/git-cinnabar/))
  * `cd` to the checked out directory.
  * Run `git am <this-repo>/firefox/0001-WIP-Firefox-source-map-spec-tests.patch`
  * Run `mach build` (this builds the test too, you'll need to run it if you modify tests/harness)
  * Run `mach test devtools/client/shared/source-map-loader/`

How to run in WebKit:
  * Check out [WebKit](https://github.com/WebKit/WebKit/)
  * `cd` to the checked out WebKit directory.
  * Run `git am <this-repo>/webkit/0001-Add-harness-for-source-maps-spec-tests.patch`
  * Run `Tools/Scripts/build-webkit` (depending on the platform you may need to pass `--gtk` or other flags)
  * Run `Tools/Scripts/run-webkit-tests LayoutTests/inspector/model/source-map-spec.html` (again, you may need `--gtk` on Linux)

Mozilla [source-map](https://github.com/mozilla/source-map) library:
  * There is a [branch](https://github.com/takikawa/source-map/tree/add-spec-tests) for adding the spec tests to the package.
