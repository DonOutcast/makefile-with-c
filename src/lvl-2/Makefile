all: print.o static main

main:
	gcc print.c -L. -lprint -o a.exe
	.\a.exe

print.o:
	gcc -c print.c

static:
	ar -rc libprint.a print.o
	ranlib libprint.a
clean:
	del *.o
	del *.a
	del *.exe