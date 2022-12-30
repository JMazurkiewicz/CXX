# C++

## Microsoft Visual Studio

### STL

Implemented C++23 features:

* [P1899R3](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p1899r3): "`stride_view`" ([#2981](https://github.com/microsoft/STL/pull/2981)),
* [P2446R2](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2446r2): "`views::as_rvalue`" ([#3008](https://github.com/microsoft/STL/pull/3008)),
* [P2278R4](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2278r4): "`cbegin` should always return a constant iterator" ([#3043](https://github.com/microsoft/STL/pull/3043), [#3187](https://github.com/microsoft/STL/pull/3187), [#3234](https://github.com/microsoft/STL/pull/3234)),
* [P2322R6](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2322r6): "`ranges::fold`" ([#3099](https://github.com/microsoft/STL/pull/3099)).

Implemented LWG issues:

* [LWG-3707](https://cplusplus.github.io/LWG/issue3707): "`chunk_view::outer-iterator::value_type::size` should return unsigned type" ([#2883](https://github.com/microsoft/STL/pull/2883)),
* [LWG-3515](https://cplusplus.github.io/LWG/issue3515): "[stacktrace.basic.nonmem]: `operator<<` should be less templatized" ([#3236](https://github.com/microsoft/STL/pull/3236)).

Fixed bugs:

* [#3113](https://github.com/microsoft/STL/pull/3113): "`<algorithm>`: `ranges::is_permutation`'s helper lambda does not specify return type".

Reported bugs:

* [#2312](https://github.com/microsoft/STL/pull/2312): "`<ranges>`: using `views::reverse` on `ranges::reverse_view` lvalue is broken",
* [#3009](https://github.com/microsoft/STL/issues/3009): "`<iterator>`: `move_sentinel` should be unwrappable",
* [#3010](https://github.com/microsoft/STL/issues/3010): "Range algorithms don't work when used with unwrappable iterators and custom sentinels",
* [StephanTLavavej#18](https://github.com/StephanTLavavej/STL/issues/18): "`<variant>`: Constructor inheritance causes ICE when class in named module inherits from class imported from `module std`",
* [StephanTLavavej#23](https://github.com/StephanTLavavej/STL/issues/23): "`<ranges>`: Usage of `ranges::iterator_t` causes ICE".

Other improvements:

* [#2696](https://github.com/microsoft/STL/pull/2696): "Update `_MSVC_STL_UPDATE` (may 2022)",
* [#3089](https://github.com/microsoft/STL/pull/3089): "Cleanup `views::as_rvalue` tests",
* [#3117](https://github.com/microsoft/STL/pull/3117): "Constexprize `bind_front` and `bind_back` tests".

### MSVC compiler

Reported bugs:

* [DevCom-10078204](https://developercommunity.visualstudio.com/t/10078204): "[C++20] (Exporting-)Importing module partition with class that inherits constructor from class imported from standard header unit causes ICE",
* [DevCom-10187107](https://developercommunity.visualstudio.com/t/10187107): "const_cast cannot be used in constexpr context".

## LLVM

### libc++

Reported bugs:

* [#58315](https://github.com/llvm/llvm-project/issues/58315): "[libc++][format] Strings are incorrectly aligned when alignment is not specified".
* [#59763](https://github.com/llvm/llvm-project/issues/59763): "[libc++][format] String literals inside of `tuple` and `pair` should be escaped"
