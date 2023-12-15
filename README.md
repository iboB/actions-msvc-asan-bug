# actions-msvc-asan-bug

Investigating a crash when using the MSVC's address sanitizer on GitHub actions.

A couple of a weeks ago (as of 2023-15-12) all executables on `windows-latest` built with msvc and `-fsanitize=address` started to crash with exit code `0xc0000142` (`STATUS_DLL_INIT_FAILED`).

Relevant [issue](https://github.com/actions/runner-images/issues/8891)
