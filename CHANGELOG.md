## 1.0.0 (2026-11-21)

### ⚠ BREAKING CHANGES

* **ui:** search result interface now includes Relevance field for scoring

* fix(types): updated import paths
* **ui:** The ResultsTable component has been refactored into smaller,
more focused components. If you were importing or extending ResultsTable directly,
you'll need to update your imports to use the new component structure.

* config: replace body line length limit rule with a disabled footer line length limit rule.

### Features

* Add automated release workflow ([333d52b](https://github.com/bharathganji/jackett-plus/commit/333d52bbe4c94ba30812a4e6fdd64ea5c5291a32))
* add fuzzy search examples to onboarding tip in SearchSuggestions ([#23](https://github.com/bharathganji/jackett-plus/issues/23)) ([7c74c70](https://github.com/bharathganji/jackett-plus/commit/7c74c700e0dd563bc522c11b049b450d5aeaf727))
* add multiple indexer search endpoint and enhance error handling ([6ea9047](https://github.com/bharathganji/jackett-plus/commit/6ea90479d417494b745f65c482b6995130ea7e22))
* Add vitest testing framework and improve search utils ([#6](https://github.com/bharathganji/jackett-plus/issues/6)) ([54dba5b](https://github.com/bharathganji/jackett-plus/commit/54dba5b102e36eed784be5c9003dd8742844fb59))
* **api:** implement result deduplication and error handling improvements ([#3](https://github.com/bharathganji/jackett-plus/issues/3)) ([362f8d5](https://github.com/bharathganji/jackett-plus/commit/362f8d51c5d1c6fca2008fcf4fcd1b72b8e85243))
* **cache:** add cookie caching for Jackett authentication ([#4](https://github.com/bharathganji/jackett-plus/issues/4)) ([6aef7a5](https://github.com/bharathganji/jackett-plus/commit/6aef7a579e329a5339e12b07f7dfe25582abf5dd))
* consolidate remaining UX improvements — leechers column, mobile layout, keyboard shortcut, filters, accessibility ([#25](https://github.com/bharathganji/jackett-plus/issues/25)) ([5d34fa0](https://github.com/bharathganji/jackett-plus/commit/5d34fa0f9bb5996154cd41f6b7663619cacefc65)), closes [#24](https://github.com/bharathganji/jackett-plus/issues/24)
* enhance caching and indexing functionality with detailed indexer support ([2aeb3a3](https://github.com/bharathganji/jackett-plus/commit/2aeb3a3923ae8ac22ea9cf69867a9ebda129e44d))
* Implement advanced fuzzy search with Fuse.js and improve UI components ([#5](https://github.com/bharathganji/jackett-plus/issues/5)) ([c675217](https://github.com/bharathganji/jackett-plus/commit/c6752177c383a6af4160735b3e9444b3c1f46130))
* **lib:** expand fuzzy search to include year, details, and indexer fields ([#26](https://github.com/bharathganji/jackett-plus/issues/26)) ([2894b8b](https://github.com/bharathganji/jackett-plus/commit/2894b8b20caaeef89681a562f16eacf8f4589125))
* **orchestration:** initialize jackett-plus open-source monorepo with CI, governance, and security ([18a3d55](https://github.com/bharathganji/jackett-plus/commit/18a3d5504466f75c2f12fba7ecec62b9347e87ec))
* refactor application structure and implement caching for indexers ([f18a4c9](https://github.com/bharathganji/jackett-plus/commit/f18a4c99ba16fc2b91ef33e448d3a17ab6c3b7c0))
* **release:** migrate to semantic-release with proper changelog support ([#16](https://github.com/bharathganji/jackett-plus/issues/16)) ([d23df0f](https://github.com/bharathganji/jackett-plus/commit/d23df0f7d388777c1a4c3c8eae0f4c8289ebb570))
* Remove ci.yml ([5bf1bd4](https://github.com/bharathganji/jackett-plus/commit/5bf1bd4cb7486b5e70633c81d05ccbfb83ea8810))
* **search:** Add recent searches functionality with dedicated hook ([6b52f42](https://github.com/bharathganji/jackett-plus/commit/6b52f420f9121724cfd1e5b4b9e8a4378d681011))
* **search:** Add recent searches functionality with dedicated hook ([#8](https://github.com/bharathganji/jackett-plus/issues/8)) ([606c45e](https://github.com/bharathganji/jackett-plus/commit/606c45e5226e11e8a42495546ae4633fa8d21a3a))
* **ui:** Add dark mode support to header logo ([#7](https://github.com/bharathganji/jackett-plus/issues/7)) ([21b4832](https://github.com/bharathganji/jackett-plus/commit/21b48321693275662bae54167bbdee6d86b24902))
* **ui:** Enhance visual design with animations and premium styling ([#9](https://github.com/bharathganji/jackett-plus/issues/9)) ([7a1b613](https://github.com/bharathganji/jackett-plus/commit/7a1b613c2f9e21ec9a7237ccbfb86d353e3ca15b))
* **ui:** implement advanced filtering and relevance-based search system ([#10](https://github.com/bharathganji/jackett-plus/issues/10)) ([bc2adb1](https://github.com/bharathganji/jackett-plus/commit/bc2adb1ea71eee84e6cce72ea278a99c68a0e93e))
* **ui:** Improve search form with clear button and enhance table performance ([0d7f3a2](https://github.com/bharathganji/jackett-plus/commit/0d7f3a2cba141b91cb46b8b0bec19639b93ebc2a))
* **ui:** modernize UI/UX architecture and continuous virtualization ([#48](https://github.com/bharathganji/jackett-plus/issues/48)) ([795457b](https://github.com/bharathganji/jackett-plus/commit/795457b285ea6c565aed4ef134052fa56d25f11e))

### Bug Fixes

* **a11y:** separate copy and open actions in search results ([#13](https://github.com/bharathganji/jackett-plus/issues/13)) ([fa0ffe0](https://github.com/bharathganji/jackett-plus/commit/fa0ffe0c22d2f60fe4dddf0e55007b72af7328e5))
* **auth:** auto-refresh expired Jackett cookies and retry on auth redirects ([e843ec4](https://github.com/bharathganji/jackett-plus/commit/e843ec4290b39f70fe2a51f99db2f8de77a8def2))
* **auth:** implement full jackett authentication flow ([#2](https://github.com/bharathganji/jackett-plus/issues/2)) ([235a4e8](https://github.com/bharathganji/jackett-plus/commit/235a4e80a7506242938cbcdb13424065bbbc23fe))
* **cache:** enhance cache initialization and detailed indexer retrieval ([dfdaaef](https://github.com/bharathganji/jackett-plus/commit/dfdaaef6fc69cb30e7fdee3c530876f2569b0930))
* **config:** rename release.config.js to .cjs for ES module compatibility ([566e26e](https://github.com/bharathganji/jackett-plus/commit/566e26e7ebf6eef7dd28ce4b2f6e2c33939a7986))
* Configure git user in auto-release workflow ([ed5e7c0](https://github.com/bharathganji/jackett-plus/commit/ed5e7c0a6d5b6809892abaffa52d0b7f7bd9ddfd))
* Delete wrangler and update packages ([#3](https://github.com/bharathganji/jackett-plus/issues/3)) ([1c3e562](https://github.com/bharathganji/jackett-plus/commit/1c3e5627871c00bc682ea18bd1e9d7db21fbffb4))
* Enhance UI/UX with softer, playful design ([#32](https://github.com/bharathganji/jackett-plus/issues/32)) ([ff47ffb](https://github.com/bharathganji/jackett-plus/commit/ff47ffb577a44845d515d78f2dc56ee9367205f2))
* minor unterminated string literal ([56444f5](https://github.com/bharathganji/jackett-plus/commit/56444f5ad64cdc85dce1980f88578bb13248cd41))
* Optimize repeated Regex compilation in search loop ([#31](https://github.com/bharathganji/jackett-plus/issues/31)) ([afad042](https://github.com/bharathganji/jackett-plus/commit/afad042a28ebef54b7fc0951c6220396d19d85fc))
* Release workflow changelog and release creation ([#14](https://github.com/bharathganji/jackett-plus/issues/14)) ([31251bb](https://github.com/bharathganji/jackett-plus/commit/31251bb7f1393e5608f6b1f2713f5ddae0dc35c4))
* **release:** remove persist-credentials to enable git push authentication ([#15](https://github.com/bharathganji/jackett-plus/issues/15)) ([4ae0299](https://github.com/bharathganji/jackett-plus/commit/4ae0299805b0e9e9f0f540f676f142c3caee74f6))
* resolve npm audit vulnerabilities via auto-fix ([#11](https://github.com/bharathganji/jackett-plus/issues/11)) ([e24751b](https://github.com/bharathganji/jackett-plus/commit/e24751b310c3c21d47b27c8356fa6801e1ecdd16))
* resolve syntax error in event_generator function ([301aeb2](https://github.com/bharathganji/jackett-plus/commit/301aeb29bdddbe23d463e3c438d6adfa4e007710))
* **search:** prevent main search input and button from filtering results ([2c89962](https://github.com/bharathganji/jackett-plus/commit/2c8996229a7950e664126d49e0bfc0f563a8aba3))
* **security:** fix potential DOM XSS via window.open ([#47](https://github.com/bharathganji/jackett-plus/issues/47)) ([a771a6e](https://github.com/bharathganji/jackett-plus/commit/a771a6e3f59c37cc659eb1d666f2317b74e40217))
* **ui:** resolve overlapping rows in results virtualizer ([#28](https://github.com/bharathganji/jackett-plus/issues/28)) ([e6a8dc9](https://github.com/bharathganji/jackett-plus/commit/e6a8dc9568f8047d4a3c09f8bd1eabe0f43ea426))
* update Node.js version to 22.x for semantic-release compatibility ([#17](https://github.com/bharathganji/jackett-plus/issues/17)) ([fd9df07](https://github.com/bharathganji/jackett-plus/commit/fd9df0789e96c2f79ff946a85486e89edb4a4aa3)), closes [#16](https://github.com/bharathganji/jackett-plus/issues/16)
* update Python version to 3.12 and fix type hints for compatibility ([96f07b0](https://github.com/bharathganji/jackett-plus/commit/96f07b04db6f406578053830bf82607a6e5debe2))
* update Python version to 3.12 and fix type hints for compatibility ([521623c](https://github.com/bharathganji/jackett-plus/commit/521623c22be67e045dec1c0fc4c2e58356c73c98))
* Update readme ([ed51253](https://github.com/bharathganji/jackett-plus/commit/ed5125336e542a6f9c39e8e8c596f10c4eb3f4d2))
* validate external indexer site links to prevent XSS ([#27](https://github.com/bharathganji/jackett-plus/issues/27)) ([fca0e3f](https://github.com/bharathganji/jackett-plus/commit/fca0e3f3888e118e745abf4bde35e3f5d5dee100))

### Performance Improvements

* **build:** Enable code splitting and optimize build configuration ([a6f9012](https://github.com/bharathganji/jackett-plus/commit/a6f9012283b726cbdf0bd5fb7d14d792e924a239))
* optimize IndexerChips filter lookup using a Set ([#40](https://github.com/bharathganji/jackett-plus/issues/40)) ([50d589f](https://github.com/bharathganji/jackett-plus/commit/50d589f4b2377176d17ed529ba50a2447ad4b4d5))
* optimize redundant lowercase computation in fuzzy search fallback ([#29](https://github.com/bharathganji/jackett-plus/issues/29)) ([b6c32c3](https://github.com/bharathganji/jackett-plus/commit/b6c32c3004e8ad770efdb99c288dccea3619907b))
* use Set for selected indexers filter ([#39](https://github.com/bharathganji/jackett-plus/issues/39)) ([92d3f03](https://github.com/bharathganji/jackett-plus/commit/92d3f03211092b31e46d965081789951fd651b03))

### Reverts

* Revert "Fix overly permissive CORS policy by restricting to trusted domains (…" ([#20](https://github.com/bharathganji/jackett-plus/issues/20)) ([7e776c7](https://github.com/bharathganji/jackett-plus/commit/7e776c7591e6190712e22de42a6f247317d27d27))
* Revert "Fix/cors vulnerability 17835525740163778925 ([#18](https://github.com/bharathganji/jackett-plus/issues/18))" ([#19](https://github.com/bharathganji/jackett-plus/issues/19)) ([26a93c1](https://github.com/bharathganji/jackett-plus/commit/26a93c197f63925df604fdd85b7bdcb423226d06))
