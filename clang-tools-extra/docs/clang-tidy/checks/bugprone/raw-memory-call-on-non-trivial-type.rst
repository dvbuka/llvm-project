.. title:: clang-tidy - bugprone-raw-memory-call-on-non-trivial-type

bugprone-raw-memory-call-on-non-trivial-type
============================================

  Flags use of the C standard library functions ``memset``, ``memcpy`` and
  ``memcmp`` and similar derivatives on non-trivial types.

  For each option, it is possible to flag extra functions that act similarly.
  Specify names in a semicolon-delimited list.
  The default is an empty string.

Options
-------

.. option:: MemSetNames

   The check will detect the following functions:
   ``memset``, ``std::memset``.

.. option:: MemCpyNames

   The check will detect the following functions:
   `std::memcpy`, ``memcpy`, `std::memmove`, ``memmove``, ``std::strcpy``,
   ``strcpy``, ``memccpy``, ``stpncpy``, ``strncpy``.

.. option:: MemCmpNames

   The check will detect the following functions:
   ``std::memcmp``, ``memcmp``, ``std::strcmp``, ``strcmp``, ``strncmp``.

This check corresponds to the CERT C++ Coding Standard rule
`OOP57-CPP. Prefer special member functions and overloaded operators to C
Standard Library functions
<https://wiki.sei.cmu.edu/confluence/display/cplusplus/OOP57-CPP.+Prefer+special+member+functions+and+overloaded+operators+to+C+Standard+Library+functions>`_.
