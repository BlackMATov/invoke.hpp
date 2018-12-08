# invoke.hpp

> std::invoke/std::apply analogs for C++14

[![travis][badge.travis]][travis]
[![appveyor][badge.appveyor]][appveyor]
[![language][badge.language]][language]
[![license][badge.license]][license]
[![paypal][badge.paypal]][paypal]

[badge.travis]: https://img.shields.io/travis/BlackMATov/invoke.hpp/master.svg?logo=travis&style=for-the-badge
[badge.appveyor]: https://img.shields.io/appveyor/ci/BlackMATov/invoke-hpp/master.svg?logo=appveyor&style=for-the-badge
[badge.language]: https://img.shields.io/badge/language-C%2B%2B14-red.svg?style=for-the-badge
[badge.license]: https://img.shields.io/badge/license-MIT-blue.svg?style=for-the-badge
[badge.paypal]: https://img.shields.io/badge/donate-PayPal-orange.svg?logo=paypal&colorA=00457C&style=for-the-badge

[travis]: https://travis-ci.org/BlackMATov/invoke.hpp
[appveyor]: https://ci.appveyor.com/project/BlackMATov/invoke-hpp
[language]: https://en.wikipedia.org/wiki/C%2B%2B14
[license]: https://en.wikipedia.org/wiki/MIT_License
[paypal]: https://www.paypal.me/matov

[invoke]: https://github.com/BlackMATov/invoke.hpp

## Installation

[invoke.hpp][invoke] is a single header library. All you need to do is copy the header file into your project and include this file:

```cpp
#include "invoke.hpp"
```

## API

### `invoke_hpp::invoke(F&& f, Args&&... args)`

Analog of [`std::invoke`](https://en.cppreference.com/w/cpp/utility/functional/invoke) from C++17

### `invoke_hpp::invoke_result<F, Args...>`

Analog of [`std::invoke_result`](https://en.cppreference.com/w/cpp/types/result_of) from C++17

### `invoke_hpp::invoke_result_t<F, Args...>`

Analog of [`std::invoke_result_t`](https://en.cppreference.com/w/cpp/types/result_of) from C++17

### `invoke_hpp::is_invocable<F, Args...>`

Analog of [`std::is_invocable`](https://en.cppreference.com/w/cpp/types/is_invocable) from C++17

### `invoke_hpp::is_invocable_r<R, F, Args...>`

Analog of [`std::is_invocable_r`](https://en.cppreference.com/w/cpp/types/is_invocable) from C++17

### `invoke_hpp::apply(F&& f, Tuple&& args)`

Analog of [`std::apply`](https://en.cppreference.com/w/cpp/utility/apply) from C++17

## [License (MIT)](./LICENSE.md)
