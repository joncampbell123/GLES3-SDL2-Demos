
all: main

LDFLAGS=`pkg-config -libs sdl2` -lGL
CXXFLAGS=`pkg-config -cflags sdl2`

main: main.o
	g++ -o main main.o $(LDFLAGS)

main.o: main.cpp
	g++ -c -o main.o main.cpp $(CXXFLAGS)

clean:
	rm -f main *.o

