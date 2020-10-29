# invoke.hpp

> std::invoke/std::apply analogs for C++11/14

[![travis][badge.travis]][travis]
[![appveyor][badge.appveyor]][appveyor]
[![codecov][badge.codecov]][codecov]
[![language][badge.language]][language]
[![license][badge.license]][license]
[![paypal][badge.paypal]][paypal]

[badge.travis]: https://img.shields.io/travis/BlackMATov/invoke.hpp/main.svg?logo=travis
[badge.appveyor]: https://img.shields.io/appveyor/ci/BlackMATov/invoke-hpp/main.svg?logo=appveyor
[badge.codecov]: https://img.shields.io/codecov/c/github/BlackMATov/invoke.hpp/main.svg?logo=codecov
[badge.language]: https://img.shields.io/badge/language-C%2B%2B11-red.svg
[badge.license]: https://img.shields.io/badge/license-MIT-blue.svg
[badge.paypal]: https://img.shields.io/badge/donate-PayPal-orange.svg?logo=paypal&colorA=00457C

[travis]: https://travis-ci.org/BlackMATov/invoke.hpp
[appveyor]: https://ci.appveyor.com/project/BlackMATov/invoke-hpp
[codecov]: https://codecov.io/gh/BlackMATov/invoke.hpp
[language]: https://en.wikipedia.org/wiki/C%2B%2B11
[license]: https://en.wikipedia.org/wiki/MIT_License
[paypal]: https://www.paypal.me/matov

[invoke]: https://github.com/BlackMATov/invoke.hpp

## Requirements

- [gcc](https://www.gnu.org/software/gcc/) **>= 4.9**
- [clang](https://clang.llvm.org/) **>= 3.8**
- [msvc](https://visualstudio.microsoft.com/) **>= 2015**

## Installation

[invoke.hpp][invoke] is a header-only library. All you need to do is copy the headers files from `headers` directory into your project and include them:

```cpp
#include "invoke.hpp/invoke.hpp"
```

Also, you can add the root repository directory to your [cmake](https://cmake.org) project:

```cmake
add_subdirectory(external/invoke.hpp)
target_link_libraries(your_project_target invoke.hpp)
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
