.PHONY: clean, rebuild
CC = gcc
CFLAGS = -Wall -Werror -Wextra -std=c11
SOURCES = print.c
OBJECTS = $(SOURCES:.c=.o)
EXECUTABLE= a.exe
LIBA = libprint.a

all: $(SOURCES)  $(EXECUTABLE) static

$(EXECUTABLE): $(OBJECTS)
	@echo hi
	$(CC) -L. -lprint $(OBJECTS) -o $@
.c:.o
	@echo hello
	$(CC)-c $(CFLAGS) $< -o $@

static:
	ar -rs $(LIBA) $(OBJECTS)
	ranlib $(LIBA)
clean:
	del *.o
	del *.a
	del *.exe
rebuild:
	make clean
	make