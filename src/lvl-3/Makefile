CC = gcc
CFLAGS =  -Wall -Werror -Wextra
LIBA = libprint.a
all: main

main: print.o
	$(CC) $(CFLAGS) print.c -L. -lprint -o a.exe

print.o: print.c print.h
	$(CC) -c  print.o

static: main
	ar -rc $(LIBA) print.o
	ranlib $(LIBA)
clean:
	rm -rf *.exe 
	rm - rf *.o