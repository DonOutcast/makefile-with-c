CC = gcc
CFLAGS =  -Wall -Werror -Wextra
LIBA = libprint.a
all: print.o static main

main:
	$(CC) $(CFLAGS) print.c -L. -lprint -o a.exe
	.\a.exe

print.o: print.c print.h
	$(CC) -c  print.c

static:
	ar -rc $(LIBA) print.o
	ranlib $(LIBA)
clean:
	del *.o 
	del *.a 
	del *.exe