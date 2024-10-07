## Template `Makefile`
```Makefile
CXX = g++
CXXFLAGS = -g -Wall

prog: main.o foo.o
      $(CXX) $(CXXFLAGS) main.o foo.o
```