## Template `Makefile`
Example Makefile:
```make
# Compiler Flags
CXX = g++
CXXFLAGS = -g -Wall

# Primary Directives
prog: main.o foo.o
	$(CXX) $(CXXFLAGS) main.o foo.o

main.o: main.cc foo.h
	$(CXX) $(CXXFLAGS) -c main.cc
      

```

**Do not ever put a header in your build directives, only ever as a dependency!**