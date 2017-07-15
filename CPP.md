# C++
Notes on C++.

## History
* [Dennis Ritchie](https://en.wikipedia.org/wiki/Dennis_Ritchie) developed C in 1972 in Bell Labs.
* [Dennis Ritchie](https://en.wikipedia.org/wiki/Dennis_Ritchie) & [Ken Thompson](https://en.wikipedia.org/wiki/Ken_Thompson) rewrote most of the unix operating system in C in 1973. 
* [The C Programming Language (K&R)](https://en.wikipedia.org/wiki/The_C_Programming_Language) was written by [Dennis Ritchie](https://en.wikipedia.org/wiki/Dennis_Ritchie) & [Brian Kernighan](https://en.wikipedia.org/wiki/Brian_Kernighan) in 1978.
* [Bjarne Stroustrup](http://www.stroustrup.com/) developed C++ in 1979 in Bell Labs.

## Compile, Link and Run
Compile and link normal C++ code using the following command:
    
    g++ -Wall hello_world.cpp -o hello_world
Important flags:
 * -Wall 
 * -W 
 * -Weffc++ 
 * -Wold-style-cast
 
 Compile and link code with important flags:
    
    g++ -Wall -W -Weffc++ -Wold-style-cast hello_world.cpp -o hello.out
    
 Run code in linux like this:
 
    ./hello.out
    
For most of my code I use this [GNU make](https://www.gnu.org/software/make/manual/make.html):

    CC := $(CXX)
    
    CXXFLAGS += -MMD -MP
    
    CXXFLAGS += -std=c++0x
    CXXFLAGS += -fdiagnostics-show-option -fmessage-length=0 -W -Wall -Werror -Weffc++
    CXXFLAGS += -Wformat=2 -Wformat-y2k
    CXXFLAGS += -Wignored-qualifiers
    CXXFLAGS += -Wmissing-include-dirs
    CXXFLAGS += -Wunused-parameter
    CXXFLAGS += -Wfloat-equal
    CXXFLAGS += -Wundef
    CXXFLAGS += -Wshadow
    CXXFLAGS += -Wpointer-arith
    CXXFLAGS += -Wcast-qual
    CXXFLAGS += -Wcast-align
    CXXFLAGS += -Wconversion
    CXXFLAGS += -Wsign-conversion
    CXXFLAGS += -Wlogical-op
    CXXFLAGS += -Wmissing-declarations
    CXXFLAGS += -Wmissing-field-initializers
    CXXFLAGS += -Wmissing-format-attribute
    CXXFLAGS += -Wredundant-decls
    
    application: application.o solution.o
    
    application.o: | run_test
    
    test: test.o solution.o
    test: LDLIBS += -lgtest -lpthread
    test: LDFLAGS += -L/usr/lib64/gtest
    
    run_test: test
            ./test
    
    clean:
            $(RM) application test *.[do]
    
     -include *.d
    
    .PHONY: clean run_test

