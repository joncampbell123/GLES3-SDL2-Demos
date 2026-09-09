
all: main

LDFLAGS=`pkg-config -libs sdl2` -lGL -lSDL2_image
CXXFLAGS=`pkg-config -cflags sdl2`

main: main.o shader.o texture.o
	g++ -o main main.o shader.o texture.o $(LDFLAGS)

main.o: main.cpp
	g++ -c -o main.o main.cpp $(CXXFLAGS)

shader.o: shader.cpp
	g++ -c -o shader.o shader.cpp $(CXXFLAGS)

texture.o: texture.cpp
	g++ -c -o texture.o texture.cpp $(CXXFLAGS)

clean:
	rm -f main *.o

