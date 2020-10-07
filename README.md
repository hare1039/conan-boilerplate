# conan-boilerplate
Boilerplate for conan. Using cmake and ninja.

# What can it do?

It is soo hard to setup an conan-enabled repo without going through the tutorial again and again. 
So this repo provide a simple boilerplate for casual use.

# What does it contain?
- A Makefile: so you can just type `make release` and it will compile your programs.
- A CMakeLists.txt: so you can manage the files that will use in your project.
- A conanfile.txt: so you can add dependency of other libraries.
- Profiles: so you can build cross-platform binary easily. Remember to edit the linux header location in Makefile.
