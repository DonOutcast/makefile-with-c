all: static
	gcc -c print.c
	gcc print.o -L. -lprint -o a.exe
	.\a.exe

static: all
	ar rc libprint.a print.o
	ranlib libprint.a