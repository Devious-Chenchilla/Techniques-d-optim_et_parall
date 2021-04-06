CC=gcc
CFLAGS=-Wall
OFLAGS=-Ofast -march=native
DFLAGS=-g3

.PHONY: all clean

all: main

main: main.o vector.o compute.o
	$(CC) -o $@ $^ $(CFLAGS) $(OFLAGS) $(DFLAGS) 

main.o: main.c compute.h
vector.o: vector.c vector.h
compute.o: compute.c vector.h timer.h compute.h

%.o: %.c
	$(CC) -c $< -o $@ $(CFLAGS) $(OFLAGS) $(DFLAGS) 

clean:
	rm -Rf *~ *.o main
