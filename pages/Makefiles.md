## Template `Makefile`
Example Makefile:
```make
# Compiler Flags
CXX = g++
CXXFLAGS = -g -Wall

# Primary Directives
prog: main.o foo.o
	$(CXX) $(CXXFLAGS) -o prog main.o foo.o

main.o: main.cc foo.h
	$(CXX) $(CXXFLAGS) -c main.cc

foo.o: foo.cc foo.h
	$(CXX) $(CXXFLAGS) -c foo.cc

```

**Do not ever put a header in your build directives, only ever as a dependency!**