# Changelog

## [0.1.0](https://github.com/mrunalC27/Img2Num/compare/bindings-c-v0.2.1...bindings-c-v0.1.0) (2026-11-20)


### ⚠ BREAKING CHANGES

* **core:** prevent holes during SVG generation ([#429](https://github.com/mrunalC27/Img2Num/issues/429))
* **core:** img2num::labels_to_svg now returns std::string instead of char*. Callers using the C++ API must update their code to capture the return value as std::string and remove any associated std::free / delete[] calls. Callers using the C binding (cimg2num) are unaffected at the ABI level but should use img2num_free_svg to deallocate the returned buffer.
* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/mrunalC27/Img2Num/issues/283))

### ✨ Features

* **library, bindings, examples:** C bindings, C & C++ shared libs, C & C++ example apps ([#263](https://github.com/mrunalC27/Img2Num/issues/263)) ([bb2403e](https://github.com/mrunalC27/Img2Num/commit/bb2403ee1a9a81f39d2b5a1746c404c3c526a2f3))
* unified image_to_svg function as complete pipeline ([#335](https://github.com/mrunalC27/Img2Num/issues/335)) ([bdba68c](https://github.com/mrunalC27/Img2Num/commit/bdba68c8adbbf79a163aba9df25849c5ff36a6b9))


### 🐛 Bug Fixes

* **bindings/c:** use (void) in error-API declarations to make them prototypes ([#764](https://github.com/mrunalC27/Img2Num/issues/764)) ([9bee27f](https://github.com/mrunalC27/Img2Num/commit/9bee27f8469596620ed73127d917bcc1d8e60b0d)), closes [#717](https://github.com/mrunalC27/Img2Num/issues/717)
* **ci:** add NPM_TOKEN to npm publish step so packages/js can ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **core:** add MSVC support via conditional compiler directives — ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **core:** prevent holes during SVG generation ([#429](https://github.com/mrunalC27/Img2Num/issues/429)) ([14e49f9](https://github.com/mrunalC27/Img2Num/commit/14e49f9a05496524e0190ddddf14283fbc907c0b))
* fix broken v0.1.0 release pipeline ([#417](https://github.com/mrunalC27/Img2Num/issues/417)) ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **gpu:** fail clearly on missing embedded shader IDs ([#813](https://github.com/mrunalC27/Img2Num/issues/813)) ([69a4f5f](https://github.com/mrunalC27/Img2Num/commit/69a4f5fb62cb34befd8a800a95819df641dab462))
* **packages/py:** include third_party/ in sdist and disable example ([2427d1d](https://github.com/mrunalC27/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* replace C++20 designated initializers with C++17 compatible assignments ([#448](https://github.com/mrunalC27/Img2Num/issues/448)) ([174b8a4](https://github.com/mrunalC27/Img2Num/commit/174b8a4b0c86bb62f929bae6e36a64896eba0f21))
* **scripts:** make `format:cpp:check` actually check without changing files ([#756](https://github.com/mrunalC27/Img2Num/issues/756)) ([589d9e9](https://github.com/mrunalC27/Img2Num/commit/589d9e9830da68dd058ad4e61521d0364e14268d)), closes [#718](https://github.com/mrunalC27/Img2Num/issues/718)


### 📚 Documentation

* refresh docs, add Python guides, and remove outdated versioning ([#446](https://github.com/mrunalC27/Img2Num/issues/446)) ([8edaadd](https://github.com/mrunalC27/Img2Num/commit/8edaadddf18ca20407b7f480cd88c72b11c99000))


### 🔧 Miscellaneous

* **.coderabbit.yml:** update to review every PR ([174b8a4](https://github.com/mrunalC27/Img2Num/commit/174b8a4b0c86bb62f929bae6e36a64896eba0f21))
* **bindings/c:** bootstrap initial release ([425ee8d](https://github.com/mrunalC27/Img2Num/commit/425ee8d89075c64f4ba99d6542a50a23c61f562c))
* bump black from 23.12.1 to 26.3.1 in the uv group across 1 directory ([#555](https://github.com/mrunalC27/Img2Num/issues/555)) ([4d6a9eb](https://github.com/mrunalC27/Img2Num/commit/4d6a9ebd37c38cdfc48543b5662df67122bb7b74))
* **ci:** add Release Please automation with multi-language publish and propagation ([#339](https://github.com/mrunalC27/Img2Num/issues/339)) ([c01bbbe](https://github.com/mrunalC27/Img2Num/commit/c01bbbeb62925487e0f9546200cfdd2ff8ed2191))
* **core:** bootstrap initial release ([f8972d6](https://github.com/mrunalC27/Img2Num/commit/f8972d6e44a4872d189d9b26af696b59f3bb9770))
* **credits:** add [@krasner](https://github.com/krasner) to author list on about page ([#301](https://github.com/mrunalC27/Img2Num/issues/301)) ([b540cd8](https://github.com/mrunalC27/Img2Num/commit/b540cd83459112ce53e8bb1990f66bc4526fef66))
* **deps-js:** update all pnpm dependencies ([#327](https://github.com/mrunalC27/Img2Num/issues/327)) ([7a2aa25](https://github.com/mrunalC27/Img2Num/commit/7a2aa2593f8dd17b21a67505494b9af286a33827))
* **main:** release bindings-c 0.1.0 ([#413](https://github.com/mrunalC27/Img2Num/issues/413)) ([2ceecb9](https://github.com/mrunalC27/Img2Num/commit/2ceecb93cf36849bf282f8db07f9b07b018d502f))
* **main:** release bindings-c 0.2.0 ([#421](https://github.com/mrunalC27/Img2Num/issues/421)) ([f3cc694](https://github.com/mrunalC27/Img2Num/commit/f3cc69454f9a195ea8f1d05c1b66bfa8ed944f64))
* **main:** release bindings-c 0.2.1 ([#545](https://github.com/mrunalC27/Img2Num/issues/545)) ([a0de888](https://github.com/mrunalC27/Img2Num/commit/a0de88828fc222693691b47339c8e6200a41840f))
* **main:** release cpp 0.3.0 ([#546](https://github.com/mrunalC27/Img2Num/issues/546)) ([147d07e](https://github.com/mrunalC27/Img2Num/commit/147d07e5f8777725d7e27d5cde515980229a3163))
* **main:** release cpp 0.4.0 ([#814](https://github.com/mrunalC27/Img2Num/issues/814)) ([7cdf6c0](https://github.com/mrunalC27/Img2Num/commit/7cdf6c0dad888a00820184c3b4fdf0ba373879f2))
* **packages/js:** bootstrap initial release ([443eb9b](https://github.com/mrunalC27/Img2Num/commit/443eb9b152b8e4c6d792e82edacc8241082cc5f4))
* **release:** add version propagation tracking files ([#787](https://github.com/mrunalC27/Img2Num/issues/787)) ([#787](https://github.com/mrunalC27/Img2Num/issues/787)) ([7d3216f](https://github.com/mrunalC27/Img2Num/commit/7d3216f61c96abb8510228961abe818b278f0740))
* **style:** update .clang-format config and reformat C/C++ sources ([#396](https://github.com/mrunalC27/Img2Num/issues/396)) ([9ca2b00](https://github.com/mrunalC27/Img2Num/commit/9ca2b0047cfc7b42ceaa3b0310806e1852119f0f))


### ♻️ Refactoring

* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/mrunalC27/Img2Num/issues/283)) ([eee9b31](https://github.com/mrunalC27/Img2Num/commit/eee9b3135b5b651a20cc8ffab74bcef073b74b6a))
* **api:** rename `ptr` to `image` ([#749](https://github.com/mrunalC27/Img2Num/issues/749)) ([080c261](https://github.com/mrunalC27/Img2Num/commit/080c2613392df13de2169ca20409ac78ca3c19b9))
* **bindings/c:** strictly conform to C++17 standard ([174b8a4](https://github.com/mrunalC27/Img2Num/commit/174b8a4b0c86bb62f929bae6e36a64896eba0f21))
* **core:** update labels_to_svg to return std::string ([#333](https://github.com/mrunalC27/Img2Num/issues/333)) ([a71e3b1](https://github.com/mrunalC27/Img2Num/commit/a71e3b17505306b96ebe56439b1f78215e53e56d))


### ✅ Tests

* add C++ and C ABI test coverage ([#702](https://github.com/mrunalC27/Img2Num/issues/702)) ([4cf8ec0](https://github.com/mrunalC27/Img2Num/commit/4cf8ec0e1ee479c9f78f6cce2665392c92271fe9))


### 🏗️ Build System

* **cmake:** distribute install rules per-target and add find_package support ([#338](https://github.com/mrunalC27/Img2Num/issues/338)) ([fce52c6](https://github.com/mrunalC27/Img2Num/commit/fce52c6779013ee13717f31000b431eb67a2ec42))
* **cmake:** refactor CMake, switch to STB submodule, use CImg2Num in WASM ([#273](https://github.com/mrunalC27/Img2Num/issues/273)) ([d929acc](https://github.com/mrunalC27/Img2Num/commit/d929acc6d158d40e4340a316ce039cbd0b1a89b4))

## [0.2.1](https://github.com/Ryan-Millard/Img2Num/compare/bindings-c-v0.2.0...bindings-c-v0.2.1) (2026-10-23)


### 🐛 Bug Fixes

* **bindings/c:** use (void) in error-API declarations to make them prototypes ([#764](https://github.com/Ryan-Millard/Img2Num/issues/764)) ([9bee27f](https://github.com/Ryan-Millard/Img2Num/commit/9bee27f8469596620ed73127d917bcc1d8e60b0d)), closes [#717](https://github.com/Ryan-Millard/Img2Num/issues/717)


### 📚 Documentation

* refresh docs, add Python guides, and remove outdated versioning ([#446](https://github.com/Ryan-Millard/Img2Num/issues/446)) ([8edaadd](https://github.com/Ryan-Millard/Img2Num/commit/8edaadddf18ca20407b7f480cd88c72b11c99000))


### 🔧 Miscellaneous

* bump black from 23.12.1 to 26.3.1 in the uv group across 1 directory ([#555](https://github.com/Ryan-Millard/Img2Num/issues/555)) ([4d6a9eb](https://github.com/Ryan-Millard/Img2Num/commit/4d6a9ebd37c38cdfc48543b5662df67122bb7b74))
* **main:** release cpp 0.3.0 ([#546](https://github.com/Ryan-Millard/Img2Num/issues/546)) ([147d07e](https://github.com/Ryan-Millard/Img2Num/commit/147d07e5f8777725d7e27d5cde515980229a3163))
* **release:** add version propagation tracking files ([#787](https://github.com/Ryan-Millard/Img2Num/issues/787)) ([#787](https://github.com/Ryan-Millard/Img2Num/issues/787)) ([7d3216f](https://github.com/Ryan-Millard/Img2Num/commit/7d3216f61c96abb8510228961abe818b278f0740))


### ♻️ Refactoring

* **api:** rename `ptr` to `image` ([#749](https://github.com/Ryan-Millard/Img2Num/issues/749)) ([080c261](https://github.com/Ryan-Millard/Img2Num/commit/080c2613392df13de2169ca20409ac78ca3c19b9))

## [0.2.0](https://github.com/Ryan-Millard/Img2Num/compare/bindings-c-v0.1.0...bindings-c-v0.2.0) (2026-06-27)


### ⚠ BREAKING CHANGES

* **core:** prevent holes during SVG generation ([#429](https://github.com/Ryan-Millard/Img2Num/issues/429))

### 🐛 Bug Fixes

* **ci:** add NPM_TOKEN to npm publish step so packages/js can authenticate and publish to the npm registry ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **core:** add MSVC support via conditional compiler directives ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **core:** prevent holes during SVG generation ([#429](https://github.com/Ryan-Millard/Img2Num/issues/429)) ([14e49f9](https://github.com/Ryan-Millard/Img2Num/commit/14e49f9a05496524e0190ddddf14283fbc907c0b))
* fix broken v0.1.0 release pipeline ([#417](https://github.com/Ryan-Millard/Img2Num/issues/417)) ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* **packages/py:** include third_party/ in sdist and disable example ([2427d1d](https://github.com/Ryan-Millard/Img2Num/commit/2427d1d3c67b9ebafcbf3a5021ed335a3d0683fc))
* replace C++20 designated initializers with C++17 compatible assignments ([#448](https://github.com/Ryan-Millard/Img2Num/issues/448)) ([174b8a4](https://github.com/Ryan-Millard/Img2Num/commit/174b8a4b0c86bb62f929bae6e36a64896eba0f21))

## 0.1.0 (2026-05-29)


### ⚠ BREAKING CHANGES

* **core:** img2num::labels_to_svg now returns std::string instead of char*. Callers using the C++ API must update their code to capture the return value as std::string and remove any associated std::free / delete[] calls. Callers using the C binding (cimg2num) are unaffected at the ABI level but should use img2num_free_svg to deallocate the returned buffer.
* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/Ryan-Millard/Img2Num/issues/283))

### ✨ Features

* **library, bindings, examples:** C bindings, C & C++ shared libs, C & C++ example apps ([#263](https://github.com/Ryan-Millard/Img2Num/issues/263)) ([bb2403e](https://github.com/Ryan-Millard/Img2Num/commit/bb2403ee1a9a81f39d2b5a1746c404c3c526a2f3))
* unified image_to_svg function as complete pipeline ([#335](https://github.com/Ryan-Millard/Img2Num/issues/335)) ([bdba68c](https://github.com/Ryan-Millard/Img2Num/commit/bdba68c8adbbf79a163aba9df25849c5ff36a6b9))


### ♻️ Refactoring

* **api:** remove draw_contour_borders from labels_to_svg ([#283](https://github.com/Ryan-Millard/Img2Num/issues/283)) ([eee9b31](https://github.com/Ryan-Millard/Img2Num/commit/eee9b3135b5b651a20cc8ffab74bcef073b74b6a))
* **core:** update labels_to_svg to return std::string ([#333](https://github.com/Ryan-Millard/Img2Num/issues/333)) ([a71e3b1](https://github.com/Ryan-Millard/Img2Num/commit/a71e3b17505306b96ebe56439b1f78215e53e56d))
