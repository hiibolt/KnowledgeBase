## Template `Makefile`
Example Makefile
```Makefile
# Compiler Flags
CXX = g++
CXXFLAGS = -g -Wall

# Primary Directives
prog: main.o foo.o
      $(CXX) $(CXXFLAGS) main.o foo.o

main.o: main.cc foo.h
      $(CXX) $(CXXFLAGS) -o main.cc
```