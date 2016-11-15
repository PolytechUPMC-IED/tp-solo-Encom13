ID3 = /home/sasl/shared/main3/env/tools
CC = g++
CFLAGS = -Wall
LDLIBS = -c

all: .o

%.o: %.cpp
	g++ -I /home/sasl/shared/main3/env/tools/include \-DVERSION="\"*{VERSION}\"" -c -o $@ $<

id3v2: %.o
	g++ -L/home/sasl/shared/main3/env/tools/lib -Wall -o id3v2 \convert.o list.o id3v2.o genre.o -lid3 -lz

clean:
	rm -f convert.o create_map.o genre.o id3v2.o list.o id3v2

install:
	nroff -man ../id3v2.1 > TP_solo/EnvDev/git/tp-solo-Encom13/man/man1/id3v2.1
