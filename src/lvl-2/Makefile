all: main

main: print.o
	gcc print.c -o a.exe

print.o: print.c print.h
	gcc -c print.c

clean:
	rm -rf *.o