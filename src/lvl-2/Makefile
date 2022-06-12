all: main

main: print.o
	gcc print.c -L. -lprint -o a.exe

print.o: print.c print.h
	gcc -c print.c

static: main print.o
	ar -rc libprint.a print.o
	ranlib libprint.a
clean:
	rm -rf *.o