
all: build static start
	
build:
	gcc -c print.c

start:
	gcc print.o -L. -lprint -o a.exe
	.\a.exe

static:
	ar rc libprint.a print.o
	ranlib libprint.a

clean:
	del *.o
	del *.a
	del *.exe