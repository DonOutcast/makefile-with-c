.PHONY: clean, rebuild
CC = gcc
CFLAGS = -Wall -Werror -Wextra -std=c11
TARGET = all
SOURCES = $(wildcard *.c)
OBJECTS = $(patsubst %.c, %.o, $(SOURCES))
EXECUTABLE= a.exe
LIBA = libprint.a

$(TARGET): $(OBJECTS) $(LIBA) $(EXECUTABLE)

$(EXECUTABLE):
	$(CC) $(CFLAGS) $(OBJECTS) -L. -lprint -o $(EXECUTABLE)
	.\$(EXECUTABLE)

.c:.o
	$(CC) $(CFLAGS) -c $< -o $@

$(LIBA):
	ar -rs $(LIBA) $(OBJECTS)
	ranlib $(LIBA)
clean:
	del *.o
	del *.a
	del *.exe
rebuild:
	make clean
	make