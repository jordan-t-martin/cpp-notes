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
- `<header.h>` is used for a first or third party library
- `"header.h"` is used for a local file

# Precompiled headers
- Used for things that change infrequently
- Needs a single cpp file to create the pch cache

# Compilation
- CPP compilation is separable, meaning they are compiled independently of each other
- Linker solves dependencies

# Visual Studio Tricks
- F12 to expand a file
- vcpkg

# lvalues and rvalues
- & means the lvalue, && means the rvalue

# Fun things
- `delete nullptr` is the same as a no-op
- Dereferencing a nullptr is undefined behavior
- Move semantics are the great defining difference of modern C++

## Keywords
- `static` means to be shared across all classes
- `explicit` applied to the constructor prevents the compiler from using that constructor for implicit conversions
# `const`
- `const` guarantees that something will not change. Can be applied to variables, pointers, or methods.
- `const int* ptr` OR `int const* ptr` means that the contents of the pointer cannot be modified
- `int* const ptr` means the pointer itself cannot be modified
- `const int* const ptr` means both the contents and the pointer cannot be modified
- `const` method means that the method will not modify any of the members of the class
- `mutable` lets you change a variable inside of a `const` method
- `inline` means to be defined one time

# Unit Testing
- `TEST_CLASS_INIT` means to execute once before any test method has ran
- `TEST_CLASS_CLEANUP` means to execute once after all test methods have ran
- Use these methods for an expensive process that needs to be done for all tests and are common across all
- `TEST_METHOD_INITIALIZE` means to execute before every individual test method
- `TEST_METHOD_CLEANUP` means to execute after every individual test method
- Tests do not always execute in serial order, so you should never depend on the order of execution when writing tests

## Classes
- `Foo a;` declares and defines the object
- Need to supply our own string...
# Rule of 6
- If you supply a constructor, you must provide ...
# Shallow vs Deep Copy Semantics
- Shallow copy just copies the pointer, also called aliasing
- Deep copy copies the contents of the pointer


