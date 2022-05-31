CC = gcc
CFLAGS = -c -Wall -Werror -Wextra

all: main

main: print.o
	$(CC) print.o -o a.exe

print.o: print.c print.h
	$(CC) $(CFLAGS)  print.c

clean:
	rm -rf *.exe 
	rm - rf *.o