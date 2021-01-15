### C++ Notes
# Guidelines
- Agreed upon document that describes the language. Compilers (such as GCC or Clang) conform to that standard. Born out of a lack of compatibility of compilers against the same codebase.

# Shared libraries
- Does not produce code, acts as a repository to hold code.
- Usd as a dependency for other projects and exectubables.
- Already compiled

## Header Files
- Purpose of a header is to share common code from other files
- Not targets of compilation
- <header.h> is used for a first or third party library
- "header.h" is used for a local file

# Precompiled headers
- Used for things that change infrequently
- Needs a single cpp file to create the pch cache

# Compilation
- CPP compilation is separable, meaning they are compiled independently of each other
- Linker solves dependencies

# Visual Studio Tricks
- F12 to expand a file

# Keywords
- static means to be shared across all classes

# Unit Testing
- TEST_CLASS_INIT means to execute once before any test method has ran
- TEST_CLASS_CLEANUP means to execute once after all test methods have ran
- TEST_METHOD_INITIALIZE means to execute before every individual test method
- TEST_METHOD_CLEANUP means to execute after every individual test method
- Tests do not always execute in serial order, so you should never depend on the order of execution when writing tests.
