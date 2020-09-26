# cppsocks : an easy to use, dependency free, header only, ASIO-free socket library.

#C++ standard required:
C++17, at minimum.

# Supported OSes:
Built and tested on Windows10 and Linux Mint (based on Ubuntu 18.04).

# External Dependencies:
None

# Why this library?
Almost all c++ socket libraries I have found have external dependencies (annoying, can be a pain to configure), or try to do too much (example: protocols such as HTTP) are built in (so you get the cruft whether you need it or not), are not header-only, look like C++ used as 'a better C', enforce weird coding styles like multiple lambda, or add 'extra stuff' like event loops or require new paradigms like 'async programming. If you need HTTP, or 'extra stuff' for your project of course you can build that on top of this library. Cppsocks does one thing and one thing only: efficiently abstracts away the creation, connection, data sending and receiving and teardown of your system's native C sockets library.

# This library is only concerned with the common tasks required to create, connect and read and write raw data. No extra cruft. If you need some protocol, you code it on top of cppsocks.

# Simple, easy to understand language use
 - You do not need to be some template meta-programming genius to use cppsocks. This style is indeed (sparingly) used in the implementation of this library, but you don't need to concern yourself with it. Instead just use the exposed classes to connect/listen and then read and write raw data.
 
# All OS-specific sockets code is hidden away in the library
 - Just use cppsocks' classes by including a couple header files in your project. They work the same in Windows or Linux.
 - For Windows, the Winsock library is automatically initialised and de-initialised for you when you use this project's classes.
 
 #
 
