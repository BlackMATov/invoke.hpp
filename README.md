# invoke.hpp

> std::invoke/std::apply analogs for C++11/14

[![linux][badge.linux]][linux]
[![darwin][badge.darwin]][darwin]
[![windows][badge.windows]][windows]
[![language][badge.language]][language]
[![license][badge.license]][license]

[badge.darwin]: https://img.shields.io/github/actions/workflow/status/BlackMATov/invoke.hpp/.github/workflows/darwin.yml?label=Xcode&logo=xcode
[badge.linux]: https://img.shields.io/github/actions/workflow/status/BlackMATov/invoke.hpp/.github/workflows/linux.yml?label=GCC%2FClang&logo=linux
[badge.windows]: https://img.shields.io/github/actions/workflow/status/BlackMATov/invoke.hpp/.github/workflows/windows.yml?label=Visual%20Studio&logo=visual-studio
[badge.language]: https://img.shields.io/badge/language-C%2B%2B11-red
[badge.license]: https://img.shields.io/badge/license-MIT-blue

[darwin]: https://github.com/BlackMATov/invoke.hpp/actions?query=workflow%3Adarwin
[linux]: https://github.com/BlackMATov/invoke.hpp/actions?query=workflow%3Alinux
[windows]: https://github.com/BlackMATov/invoke.hpp/actions?query=workflow%3Awindows
[language]: https://en.wikipedia.org/wiki/C%2B%2B11
[license]: https://en.wikipedia.org/wiki/MIT_License

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
target_link_libraries(your_project_target PUBLIC invoke.hpp::invoke.hpp)
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
