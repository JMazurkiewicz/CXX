# C++

## Microsoft Visual Studio

### STL

Implemented C++23 features:

* [P1899R3](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p1899r3): "`stride_view`" ([#2981](https://github.com/microsoft/STL/pull/2981)),
* [P2446R2](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2446r2): "`views::as_rvalue`" ([#3008](https://github.com/microsoft/STL/pull/3008)),
* [P2278R4](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2278r4): "`cbegin` should always return a constant iterator" ([#3043](https://github.com/microsoft/STL/pull/3043), [#3187](https://github.com/microsoft/STL/pull/3187), [#3234](https://github.com/microsoft/STL/pull/3234)),
* [P2322R6](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2322r6): "`ranges::fold`" ([#3099](https://github.com/microsoft/STL/pull/3099)),
* [P2165R4](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2165r4.pdf): "Compatibility between `tuple`, `pair` and *tuple-like* objects" ([#3323](https://github.com/microsoft/STL/pull/3323), [#3372](https://github.com/microsoft/STL/pull/3372)),
* [P2404R3](https://wg21.link/P2404R3): "Move-only types for `equality_comparable_with`, `totally_ordered_with`, and `three_way_comparable_with`" ([#3345](https://github.com/microsoft/STL/pull/3345)),
* [P2164R9](https://wg21.link/P2164R9): "`views::enumerate`" ([#3472](https://github.com/microsoft/STL/pull/3472)),
* [P2609R3](https://wg21.link/P2609R3): "Relaxing Ranges Just A Smidge" ([#3486](https://github.com/microsoft/STL/pull/3486)),
* [P2321R2](https://wg21.link/P2321R2): "`zip`" (partial: [#3508](https://github.com/microsoft/STL/pull/3508), [#3546](https://github.com/microsoft/STL/pull/3546)),
* [P0009R18](https://wg21.link/P0009R18): "MDSPAN" (partial: [#3534](https://github.com/microsoft/STL/pull/3534), [#3535](https://github.com/microsoft/STL/pull/3535), [#3560](https://github.com/microsoft/STL/pull/3560), [#3564](https://github.com/microsoft/STL/pull/3564), [#3580](https://github.com/microsoft/STL/pull/3580)),
* [P2736R2](https://wg21.link/P2736R2): "Referencing The Unicode Standard" ([#3556](https://github.com/microsoft/STL/pull/3556)),
* [P2374R4](https://wg21.link/P2374R4): "`views::cartesian_product`" ([#3561](https://github.com/microsoft/STL/pull/3561)).

Implemented LWG issues:

* [LWG-3707](https://cplusplus.github.io/LWG/issue3707): "`chunk_view::outer-iterator::value_type::size` should return unsigned type" ([#2883](https://github.com/microsoft/STL/pull/2883)),
* [LWG-3515](https://cplusplus.github.io/LWG/issue3515): "[stacktrace.basic.nonmem]: `operator<<` should be less templatized" ([#3236](https://github.com/microsoft/STL/pull/3236)),
* [LWG-3810](https://cplusplus.github.io/LWG/issue3810): "CTAD for `basic_format_args`" ([#3421](https://github.com/microsoft/STL/pull/3421)),
* [LWG-3848](https://cplusplus.github.io/LWG/issue3848): "`slide_view` missing `base` accessor" ([#3410](https://github.com/microsoft/STL/pull/3410)),
* [LWG-3850](https://cplusplus.github.io/LWG/issue3850): "`views::as_const` on `empty_view<T>` should return `empty_view<const T>`" ([#3423](https://github.com/microsoft/STL/pull/3423)),
* [LWG-3851](https://cplusplus.github.io/LWG/issue3851): "`chunk_view::inner-iterator` missing custom `iter_move` and `iter_swap`" ([#3517](https://github.com/microsoft/STL/pull/3517)),
* [LWG-3853](https://cplusplus.github.io/LWG/issue3853): "`basic_const_iterator<volatile int*>::operator->` is ill-formed" ([#3468](https://github.com/microsoft/STL/pull/3468)),
* [LWG-3862](https://cplusplus.github.io/LWG/issue3862): "`basic_const_iterator`'s `common_type` specialization is underconstrained" ([#3471](https://github.com/microsoft/STL/pull/3471)),
* [LWG-3872](https://cplusplus.github.io/LWG/issue3872): "`basic_const_iterator` should have custom `iter_move`" ([#3470](https://github.com/microsoft/STL/pull/3470)),
* [LWG-3875](https://cplusplus.github.io/LWG/issue3875): "`std::ranges::repeat_view<T, IntegerClass>::iterator` may be ill-formed" ([#3485](https://github.com/microsoft/STL/pull/3485)),
* [LWG-3880](https://cplusplus.github.io/LWG/issue3880): "Clarify `operator+=` complexity for `{chunk,stride}_view::iterator`" ([#3554](https://github.com/microsoft/STL/pull/3554)).

Fixed bugs:

* [#3113](https://github.com/microsoft/STL/pull/3113): "`<algorithm>`: `ranges::is_permutation`'s helper lambda does not specify return type",
* [#3380](https://github.com/microsoft/STL/pull/3380): "`<system_error>`: Use uglified `[[clang::require_constant_initialization]]` attribute",
* [#3493](https://github.com/microsoft/STL/pull/3493): "`<ranges>`: Fix misused list-initializations",
* [#3551](https://github.com/microsoft/STL/pull/3551): "`<ranges>`: Fix `ranges::equal` for ranges with integer-class `range_difference_t`".

Reported bugs:

* [#2312](https://github.com/microsoft/STL/pull/2312): "`<ranges>`: using `views::reverse` on `ranges::reverse_view` lvalue is broken",
* [#3009](https://github.com/microsoft/STL/issues/3009): "`<iterator>`: `move_sentinel` should be unwrappable",
* [#3010](https://github.com/microsoft/STL/issues/3010): "Range algorithms don't work when used with unwrappable iterators and custom sentinels",
* [#3392](https://github.com/microsoft/STL/issues/3392): "`<ranges>`: `views::repeat(...) | views::take(...)` is not always a valid range" (fixed by [#3485](https://github.com/microsoft/STL/pull/3485)),
* [#3550](https://github.com/microsoft/STL/issues/3550): "`<ranges>`: `ranges::equal` does not work for ranges with integer-class `range_difference_t`" (fixed by [#3551](https://github.com/microsoft/STL/pull/3551)),
* [StephanTLavavej/STL#18](https://github.com/StephanTLavavej/STL/issues/18): "`<variant>`: Constructor inheritance causes ICE when class in named module inherits from class imported from `module std`",
* [StephanTLavavej/STL#23](https://github.com/StephanTLavavej/STL/issues/23): "`<ranges>`: Usage of `ranges::iterator_t` causes ICE".

Other improvements:

* [#2696](https://github.com/microsoft/STL/pull/2696): "Update `_MSVC_STL_UPDATE` (may 2022)",
* [#3089](https://github.com/microsoft/STL/pull/3089): "Cleanup `views::as_rvalue` tests",
* [#3117](https://github.com/microsoft/STL/pull/3117): "Constexprize `bind_front` and `bind_back` tests",
* [#3350](https://github.com/microsoft/STL/pull/3350): "Improve `views::elements` tests",
* [#3390](https://github.com/microsoft/STL/pull/3390): "Improve `views::drop(_while)` and `views::take(_while)` tests",
* [#3391](https://github.com/microsoft/STL/issues/3391): "`<ranges>`: Add missing test coverage for `ranges::view_interface::c(begin|end)`",
* [#3553](https://github.com/microsoft/STL/pull/3553): "`<ranges>`: Test `c(begin|end)` members of range factories".

### MSVC compiler

Reported bugs:

* [DevCom-10078204](https://developercommunity.visualstudio.com/t/10078204): "[C++20] (Exporting-)Importing module partition with class that inherits constructor from class imported from standard header unit causes ICE",
* [DevCom-10187107](https://developercommunity.visualstudio.com/t/10187107): "const_cast cannot be used in constexpr context",
* [DevCom-10269323](https://developercommunity.visualstudio.com/t/10269323): "[C++] Post-increment operator cannot refer to `this` pointer in `noexcept` specifier".

## LLVM

### libc++

Implemented C++23 features:

* [P2443R1](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2021/p2443r1.html): "\[libc++][ranges] Implement P2443R1: `views::chunk_by`" (WIP: [D144767](https://reviews.llvm.org/D144767)).

Reported bugs:

* [#58315](https://github.com/llvm/llvm-project/issues/58315): "\[libc++][format] Strings are incorrectly aligned when alignment is not specified",
* [#59763](https://github.com/llvm/llvm-project/issues/59763): "\[libc++][format] String literals inside of `tuple` and `pair` should be escaped",
* [#60123](https://github.com/llvm/llvm-project/issues/60123): "\[libc++][format] Negation of `LLONG_MIN` (UB) when formatting `chrono::duration`",
* [#60164](https://github.com/llvm/llvm-project/issues/60164): "\[libc++][format] Some contiguous ranges cannot be formatted due to lack of `data` or `size` member functions",
* [#60658](https://github.com/llvm/llvm-project/issues/60658): "\[libc++][ranges] `views::drop` uses non-reserved identifiers `dist` and `clamped`",
* [#60986](https://github.com/llvm/llvm-project/issues/60986): "\[libc++][ranges] Feature test macro for `views::as_rvalue` is missing",
* [#61314](https://github.com/llvm/llvm-project/issues/61314): "\[libc++][format] Should `formatter<vec-bool-ref>` be default constructible without `<format>` include?".

### Clang

Reported bugs:

* [#59827](https://github.com/llvm/llvm-project/issues/59827): "\[Clang][concepts] Conditional explicit specifier is checked too early in constrained constructor".
