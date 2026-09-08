
all: main

LDFLAGS=`pkg-config -libs sdl2` -lGL
CXXFLAGS=`pkg-config -cflags sdl2`

main: main.o shader.o
	g++ -o main main.o shader.o $(LDFLAGS)

main.o: main.cpp
	g++ -c -o main.o main.cpp $(CXXFLAGS)

shader.o: shader.cpp
	g++ -c -o shader.o shader.cpp $(CXXFLAGS)

clean:
	rm -f main *.o

