WIP repo for source map test proof of concept
---------------------------------------------

How to run in Firefox:
  * Check out mozilla-unified (see [Firefox dev setup](https://firefox-source-docs.mozilla.org/setup/index.html) for details, note that you can use git via [git-cinnabar](https://github.com/glandium/git-cinnabar/))
  * Change to the checked out directory.
  * `git am <this-repo>/firefox/0001-WIP-Firefox-source-map-spec-tests.patch`
  * `mach build`
  * `mach test devtools/client/shared/source-map-loader/`

How to run in WebKit:
  * Check out [WebKit](https://github.com/WebKit/WebKit/)
  * `git am <this-repo>/webkit/0001-Add-harness-for-source-maps-spec-tests.patch`
  * Change to the WebKit directory.
  * Run `Tools/Scripts/build-webkit` (depending on the platform you may need to pass `--gtk` or other flags)
  * Run `run-webkit-tests LayoutTests/inspector/model/source-map-spec.html` (again, you may need `--gtk` on Linux)
