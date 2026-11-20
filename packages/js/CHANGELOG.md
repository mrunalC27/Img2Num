# Changelog

## [0.1.0](https://github.com/mrunalC27/Img2Num/compare/packages-js-v0.4.2...packages-js-v0.1.0) (2026-11-20)


### ⚠ BREAKING CHANGES

* **js:** img2num no longer offloads WASM execution to a background thread automatically. Heavy operations (gaussianBlur, bilateralFilter, kmeans, imageToSvg) now run on whichever thread calls them. This can block the calling thread (browser main thread/UI or the Node event loop during processing. Consumers who need non-blocking behavior must now wrap calls in their own Worker or worker_thread.
* **core:** prevent holes during SVG generation ([#429](https://github.com/mrunalC27/Img2Num/issues/429))
* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/mrunalC27/Img2Num/issues/283))

### ✨ Features

* **Debug Logging:** route logging through spdlog with compile-time level control ([#524](https://github.com/mrunalC27/Img2Num/issues/524)) ([47c8dd9](https://github.com/mrunalC27/Img2Num/commit/47c8dd91a8325a1f7f34838b978a8830f5f839b6))
* **example app:** add html-js example app to demo basic library usage ([72c4669](https://github.com/mrunalC27/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))
* **Types:** Ship TypeScript type definitions for the npm package ([#670](https://github.com/mrunalC27/Img2Num/issues/670)) ([b2dbed8](https://github.com/mrunalC27/Img2Num/commit/b2dbed84618020b89b507d70528a82a416faa9ad)), closes [#631](https://github.com/mrunalC27/Img2Num/issues/631)
* unified image_to_svg function as complete pipeline ([#335](https://github.com/mrunalC27/Img2Num/issues/335)) ([bdba68c](https://github.com/mrunalC27/Img2Num/commit/bdba68c8adbbf79a163aba9df25849c5ff36a6b9))


### 🐛 Bug Fixes

* **ci:** add NPM_TOKEN to npm publish step so packages/js can ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **commonjs:** load webgpu via dynamic import, fall back to CPU, and guard the CJS build ([#562](https://github.com/mrunalC27/Img2Num/issues/562)) ([e44480d](https://github.com/mrunalC27/Img2Num/commit/e44480d9c4736c1ae67094a121731ae9adc4365b))
* **core:** add MSVC support via conditional compiler directives — ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **core:** prevent holes during SVG generation ([#429](https://github.com/mrunalC27/Img2Num/issues/429)) ([14e49f9](https://github.com/mrunalC27/Img2Num/commit/14e49f9a05496524e0190ddddf14283fbc907c0b))
* fix broken v0.1.0 release pipeline ([#417](https://github.com/mrunalC27/Img2Num/issues/417)) ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **ImageToUint8Array:** memory leak and silent failure ([#487](https://github.com/mrunalC27/Img2Num/issues/487)) ([0eb0598](https://github.com/mrunalC27/Img2Num/commit/0eb0598ec64ce6859946f79b89a554da87717f9c))
* **packages/js:** Remote property injection in wasmWorker.js ([#346](https://github.com/mrunalC27/Img2Num/issues/346)) ([dfe3afe](https://github.com/mrunalC27/Img2Num/commit/dfe3afe55dc380c89e9d8cb38df350a178ee3caf))
* **packages/js:** support browser and node builds from shared Vite setup ([#449](https://github.com/mrunalC27/Img2Num/issues/449)) ([0b2467c](https://github.com/mrunalC27/Img2Num/commit/0b2467c672474ef438f17ade91bfb7ed966632ca))
* **packages/py:** include third_party/ in sdist and disable example ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* restore static wasm URL for bundler asset detection ([#559](https://github.com/mrunalC27/Img2Num/issues/559)) ([1a27346](https://github.com/mrunalC27/Img2Num/commit/1a2734629701a702d7e7d5294fe8a8199187412b))


### ⚡ Performance Improvements

* **gpu:** add WebGPU acceleration with automatic fallback to CPU ([#272](https://github.com/mrunalC27/Img2Num/issues/272)) ([c385319](https://github.com/mrunalC27/Img2Num/commit/c3853198aaf72e00888352653bf44fe129261201))


### 📚 Documentation

* add JS 0.4.2 blog post, overhaul READMEs and security policy, redesign navbar ([#558](https://github.com/mrunalC27/Img2Num/issues/558)) ([e1a2a8a](https://github.com/mrunalC27/Img2Num/commit/e1a2a8aa332dc0a3e826a80e2ac9581964f747f5))
* **api:** describe black_threshold_image as a per-channel brightness cutoff ([#692](https://github.com/mrunalC27/Img2Num/issues/692)) ([3506b0a](https://github.com/mrunalC27/Img2Num/commit/3506b0afc82b6d67e69e38a906b0cbf91763fb20)), closes [#691](https://github.com/mrunalC27/Img2Num/issues/691)
* **CSS:** fix table of contents styling and layout ([72c4669](https://github.com/mrunalC27/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))
* **examples:** add community showcase ([#644](https://github.com/mrunalC27/Img2Num/issues/644)) ([e6b20ba](https://github.com/mrunalC27/Img2Num/commit/e6b20babd1bd7d66662b25435e0297155605f10c)), closes [#638](https://github.com/mrunalC27/Img2Num/issues/638)
* **JSDoc:** fix inaccurate [@throws](https://github.com/throws) and remove stale [@todo](https://github.com/todo) in imageToUint8ClampedArray ([#802](https://github.com/mrunalC27/Img2Num/issues/802)) ([c5ef4c3](https://github.com/mrunalC27/Img2Num/commit/c5ef4c3e1f83164d014c00aebd3b9a67a6d45106)), closes [#671](https://github.com/mrunalC27/Img2Num/issues/671)
* **packages/js:** add README for npm package ([#466](https://github.com/mrunalC27/Img2Num/issues/466)) ([f193a54](https://github.com/mrunalC27/Img2Num/commit/f193a543f872b60a735706c1b5c1d6671c31563b))
* **README.md:** add alt attributes to language icons and badges ([#498](https://github.com/mrunalC27/Img2Num/issues/498)) ([21cf395](https://github.com/mrunalC27/Img2Num/commit/21cf39517785890cb7970e6e351b095558f85d87)), closes [#492](https://github.com/mrunalC27/Img2Num/issues/492)
* update JSDoc comments and break up website docs ([72c4669](https://github.com/mrunalC27/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))
* **website:** added the Discord server to the navbar, footer and contributing guide ([#689](https://github.com/mrunalC27/Img2Num/issues/689)) ([2d7e84d](https://github.com/mrunalC27/Img2Num/commit/2d7e84defce9e4f6ea3b17cd7f4a29732f03d41d))
* **website:** update documentation based on refactor in [#510](https://github.com/mrunalC27/Img2Num/issues/510) ([72c4669](https://github.com/mrunalC27/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))


### 🔧 Miscellaneous

* add CHANGELOG.md to the package files whitelist ([1a27346](https://github.com/mrunalC27/Img2Num/commit/1a2734629701a702d7e7d5294fe8a8199187412b))
* **bindings/c:** bootstrap initial release ([425ee8d](https://github.com/mrunalC27/Img2Num/commit/425ee8d89075c64f4ba99d6542a50a23c61f562c))
* bump @rollup/plugin-commonjs from 28.0.9 to 29.0.3 in /packages/js in the all-deps group across 1 directory ([#563](https://github.com/mrunalC27/Img2Num/issues/563)) ([dcf2eba](https://github.com/mrunalC27/Img2Num/commit/dcf2ebac0ace0acabb0c3c03cf4af8d991ad500f))
* bump black from 23.12.1 to 26.3.1 in the uv group across 1 directory ([#555](https://github.com/mrunalC27/Img2Num/issues/555)) ([4d6a9eb](https://github.com/mrunalC27/Img2Num/commit/4d6a9ebd37c38cdfc48543b5662df67122bb7b74))
* bump the all-deps group across 1 directory with 18 updates ([#474](https://github.com/mrunalC27/Img2Num/issues/474)) ([02a6934](https://github.com/mrunalC27/Img2Num/commit/02a6934aaae91790335b2cfdecb31b2f2236c628))
* bump the all-deps group across 1 directory with 21 dep and 3 toolchain updates ([#604](https://github.com/mrunalC27/Img2Num/issues/604)) ([463ad7a](https://github.com/mrunalC27/Img2Num/commit/463ad7ab4c45d17b987e7c89d514fee467f48b23))
* **ci:** add Release Please automation with multi-language publish and propagation ([#339](https://github.com/mrunalC27/Img2Num/issues/339)) ([c01bbbe](https://github.com/mrunalC27/Img2Num/commit/c01bbbeb62925487e0f9546200cfdd2ff8ed2191))
* **core:** bootstrap initial release ([f8972d6](https://github.com/mrunalC27/Img2Num/commit/f8972d6e44a4872d189d9b26af696b59f3bb9770))
* **deps-js:** update all pnpm dependencies ([#327](https://github.com/mrunalC27/Img2Num/issues/327)) ([7a2aa25](https://github.com/mrunalC27/Img2Num/commit/7a2aa2593f8dd17b21a67505494b9af286a33827))
* **deps:** bump docs, example-apps and packages/js devDependencies ([#576](https://github.com/mrunalC27/Img2Num/issues/576)) ([8bda4a3](https://github.com/mrunalC27/Img2Num/commit/8bda4a3adb564c453b7fe4a7b86d0d182e69f7a3))
* **js:** ship multi-format artifacts (browser ESM, standalone UMD/IIFE, node ESM/CJS) ([f5b1ef9](https://github.com/mrunalC27/Img2Num/commit/f5b1ef907e43b68c32bdc15238daae6f28edf40f))
* **main:** release bindings-c 0.2.1 ([#545](https://github.com/mrunalC27/Img2Num/issues/545)) ([a0de888](https://github.com/mrunalC27/Img2Num/commit/a0de88828fc222693691b47339c8e6200a41840f))
* **main:** release packages-js 0.1.0 ([#412](https://github.com/mrunalC27/Img2Num/issues/412)) ([2ed9eb9](https://github.com/mrunalC27/Img2Num/commit/2ed9eb9ccde3dcb0a22b48ccd33b697d91f9f9bd))
* **main:** release packages-js 0.2.0 ([#419](https://github.com/mrunalC27/Img2Num/issues/419)) ([973ab65](https://github.com/mrunalC27/Img2Num/commit/973ab6512708ccaa8a60471f29e36cddd3ebbcb8))
* **main:** release packages-js 0.2.1 ([#493](https://github.com/mrunalC27/Img2Num/issues/493)) ([8efd2cd](https://github.com/mrunalC27/Img2Num/commit/8efd2cd4072f3705db7d2e93c1be5432faac65f2))
* **main:** release packages-js 0.3.0 ([0da1a3a](https://github.com/mrunalC27/Img2Num/commit/0da1a3a6270a920c528ad0785d50682b090188f5))
* **main:** release packages-js 0.4.0 ([#554](https://github.com/mrunalC27/Img2Num/issues/554)) ([f276500](https://github.com/mrunalC27/Img2Num/commit/f276500ef04a5df0fadde5c9b73d699a4cb6ba2d))
* **main:** release packages-js 0.4.1 ([#561](https://github.com/mrunalC27/Img2Num/issues/561)) ([f71c8f9](https://github.com/mrunalC27/Img2Num/commit/f71c8f9a7856e46eef789b56995f24a9138c8436))
* **main:** release packages-js 0.4.2 ([#567](https://github.com/mrunalC27/Img2Num/issues/567)) ([f999994](https://github.com/mrunalC27/Img2Num/commit/f99999473ccad5eb7b94ff0af9ed8188d26bc314))
* **monorepo:** refactor entire project to monorepo and setup initial JS package ([#250](https://github.com/mrunalC27/Img2Num/issues/250)) ([4570048](https://github.com/mrunalC27/Img2Num/commit/4570048cd3b14e57b442e19693eef85ba3e859c7))
* **packages/js:** bootstrap initial release ([443eb9b](https://github.com/mrunalC27/Img2Num/commit/443eb9b152b8e4c6d792e82edacc8241082cc5f4))
* **packages/js:** explicitly include only the required build-wasm files ([#393](https://github.com/mrunalC27/Img2Num/issues/393)) ([b7207b0](https://github.com/mrunalC27/Img2Num/commit/b7207b064dccd919644bf4633816998ef36ff4fd))
* **release:** add version propagation tracking files ([#787](https://github.com/mrunalC27/Img2Num/issues/787)) ([#787](https://github.com/mrunalC27/Img2Num/issues/787)) ([7d3216f](https://github.com/mrunalC27/Img2Num/commit/7d3216f61c96abb8510228961abe818b278f0740))
* split justfile ([#695](https://github.com/mrunalC27/Img2Num/issues/695)) ([9fa8c0f](https://github.com/mrunalC27/Img2Num/commit/9fa8c0f288254306417e5b92e81bf5fd9bb8319b))
* **urls:** migrate documentation and site links to img2num.dev ([#496](https://github.com/mrunalC27/Img2Num/issues/496)) ([af0ac79](https://github.com/mrunalC27/Img2Num/commit/af0ac79d52afdca848f56768d8ff4ed97ba4b07c))


### ♻️ Refactoring

* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/mrunalC27/Img2Num/issues/283)) ([eee9b31](https://github.com/mrunalC27/Img2Num/commit/eee9b3135b5b651a20cc8ffab74bcef073b74b6a))
* **docs:** make Docusaurus site the primary site, move React example to /example-apps/react-js/ ([#486](https://github.com/mrunalC27/Img2Num/issues/486)) ([a235ec5](https://github.com/mrunalC27/Img2Num/commit/a235ec52db1fec3af0aa08b305e91f9a78b8945f))
* **js:** make TARGET lookup a strict allowlist ([#590](https://github.com/mrunalC27/Img2Num/issues/590)) ([0d3a0cb](https://github.com/mrunalC27/Img2Num/commit/0d3a0cb8ff1f53fd22d4555974430a0d4fc150a0)), closes [#580](https://github.com/mrunalC27/Img2Num/issues/580)
* **js:** run WASM calls on the caller's thread instead of a Worker ([#510](https://github.com/mrunalC27/Img2Num/issues/510)) ([72c4669](https://github.com/mrunalC27/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))


### 🏗️ Build System

* **cmake:** refactor CMake, switch to STB submodule, use CImg2Num in WASM ([#273](https://github.com/mrunalC27/Img2Num/issues/273)) ([d929acc](https://github.com/mrunalC27/Img2Num/commit/d929acc6d158d40e4340a316ce039cbd0b1a89b4))

## [0.4.2](https://github.com/Ryan-Millard/Img2Num/compare/packages-js-v0.4.1...packages-js-v0.4.2) (2026-08-18)


### 🐛 Bug Fixes

* **commonjs:** load webgpu via dynamic import, fall back to CPU, and guard the CJS build ([#562](https://github.com/Ryan-Millard/Img2Num/issues/562)) ([e44480d](https://github.com/Ryan-Millard/Img2Num/commit/e44480d9c4736c1ae67094a121731ae9adc4365b))

## [0.4.1](https://github.com/Ryan-Millard/Img2Num/compare/packages-js-v0.4.0...packages-js-v0.4.1) (2026-08-16)


### 🐛 Bug Fixes

* restore static wasm URL for bundler asset detection ([#559](https://github.com/Ryan-Millard/Img2Num/issues/559)) ([1a27346](https://github.com/Ryan-Millard/Img2Num/commit/1a2734629701a702d7e7d5294fe8a8199187412b))

## [0.4.0](https://github.com/Ryan-Millard/Img2Num/compare/packages-js-v0.3.0...packages-js-v0.4.0) (2026-08-16)


### ⚠ BREAKING CHANGES

* **js:** dist layout and filenames have changed. Artifacts now live at dist/browser/img2num.js, dist/standalone/img2num.umd.js, dist/standalone/img2num.iife.js, and dist/node/img2num.{js,cjs}; deep imports into dist/ must be updated. Export conditions are reordered so bundlers targeting the browser resolve the browser build (they previously matched "import" first and received the node build). Minimum supported Node is now 18.

### ✨ Features

* **js:** ship multi-format artifacts (browser ESM, standalone UMD/IIFE, node ESM/CJS) ([#530](https://github.com/Ryan-Millard/Img2Num/issues/530)) ([f5b1ef9](https://github.com/Ryan-Millard/Img2Num/commit/f5b1ef907e43b68c32bdc15238daae6f28edf40f))


### 📚 Documentation

* **website:** add example apps index page and rebuild HTML demos from a shared template ([f5b1ef9](https://github.com/Ryan-Millard/Img2Num/commit/f5b1ef907e43b68c32bdc15238daae6f28edf40f))

## [0.3.0](https://github.com/Ryan-Millard/Img2Num/compare/packages-js-v0.2.1...packages-js-v0.3.0) (2026-07-31)


### ⚠ BREAKING CHANGES

* **js:** img2num no longer offloads WASM execution to a background thread automatically. Heavy operations (gaussianBlur, bilateralFilter, kmeans, imageToSvg) now run on whichever thread calls them. This can block the calling thread (browser main thread/UI or the Node event loop during processing. Consumers who need non-blocking behavior must now wrap calls in their own Worker or worker_thread.

### ✨ Features

* **example app:** add html-js example app to demo basic library usage ([72c4669](https://github.com/Ryan-Millard/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))


### 📚 Documentation

* **CSS:** fix table of contents styling and layout ([72c4669](https://github.com/Ryan-Millard/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))
* **README.md:** add alt attributes to language icons and badges ([#498](https://github.com/Ryan-Millard/Img2Num/issues/498)) ([21cf395](https://github.com/Ryan-Millard/Img2Num/commit/21cf39517785890cb7970e6e351b095558f85d87)), closes [#492](https://github.com/Ryan-Millard/Img2Num/issues/492)
* update JSDoc comments and break up website docs ([72c4669](https://github.com/Ryan-Millard/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))
* **website:** update documentation based on refactor in [#510](https://github.com/Ryan-Millard/Img2Num/issues/510) ([72c4669](https://github.com/Ryan-Millard/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))


### ♻️ Refactoring

* **js:** run WASM calls on the caller's thread instead of a Worker ([#510](https://github.com/Ryan-Millard/Img2Num/issues/510)) ([72c4669](https://github.com/Ryan-Millard/Img2Num/commit/72c466913d2ea0d33f910eeffb5e87ab0b463beb))

## [0.2.1](https://github.com/Ryan-Millard/Img2Num/compare/packages-js-v0.2.0...packages-js-v0.2.1) (2026-07-05)


### 🐛 Bug Fixes

* **ImageToUint8Array:** memory leak and silent failure ([#487](https://github.com/Ryan-Millard/Img2Num/issues/487)) ([0eb0598](https://github.com/Ryan-Millard/Img2Num/commit/0eb0598ec64ce6859946f79b89a554da87717f9c))


### 📚 Documentation

* **packages/js:** add README for npm package ([#466](https://github.com/Ryan-Millard/Img2Num/issues/466)) ([f193a54](https://github.com/Ryan-Millard/Img2Num/commit/f193a543f872b60a735706c1b5c1d6671c31563b))

## [0.2.0](https://github.com/Ryan-Millard/Img2Num/compare/packages-js-v0.1.0...packages-js-v0.2.0) (2026-06-27)


### ⚠ BREAKING CHANGES

* **core:** prevent holes during SVG generation ([#429](https://github.com/Ryan-Millard/Img2Num/issues/429))

### 🐛 Bug Fixes

* **ci:** add NPM_TOKEN to npm publish step so packages/js can authenticate and publish to the npm registry ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **core:** add MSVC support via conditional compiler directives ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **core:** prevent holes during SVG generation ([#429](https://github.com/Ryan-Millard/Img2Num/issues/429)) ([14e49f9](https://github.com/Ryan-Millard/Img2Num/commit/14e49f9a05496524e0190ddddf14283fbc907c0b))
* fix broken v0.1.0 release pipeline ([#417](https://github.com/Ryan-Millard/Img2Num/issues/417)) ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **packages/js:** support browser and node builds from shared Vite setup ([#449](https://github.com/Ryan-Millard/Img2Num/issues/449)) ([0b2467c](https://github.com/Ryan-Millard/Img2Num/commit/0b2467c672474ef438f17ade91bfb7ed966632ca))
* **packages/py:** include third_party/ in sdist and disable example ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))

## 0.1.0 (2026-05-29)


### ⚠ BREAKING CHANGES

* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/Ryan-Millard/Img2Num/issues/283))

### ✨ Features

* unified image_to_svg function as complete pipeline ([#335](https://github.com/Ryan-Millard/Img2Num/issues/335)) ([bdba68c](https://github.com/Ryan-Millard/Img2Num/commit/bdba68c8adbbf79a163aba9df25849c5ff36a6b9))


### 🐛 Bug Fixes

* **packages/js:** Remote property injection in wasmWorker.js ([#346](https://github.com/Ryan-Millard/Img2Num/issues/346)) ([dfe3afe](https://github.com/Ryan-Millard/Img2Num/commit/dfe3afe55dc380c89e9d8cb38df350a178ee3caf))


### ⚡ Performance Improvements

* **gpu:** add WebGPU acceleration with automatic fallback to CPU ([#272](https://github.com/Ryan-Millard/Img2Num/issues/272)) ([c385319](https://github.com/Ryan-Millard/Img2Num/commit/c3853198aaf72e00888352653bf44fe129261201))


### ♻️ Refactoring

* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/Ryan-Millard/Img2Num/issues/283)) ([eee9b31](https://github.com/Ryan-Millard/Img2Num/commit/eee9b3135b5b651a20cc8ffab74bcef073b74b6a))
