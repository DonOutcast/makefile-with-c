.PHONY: clean, rebuild
CC = gcc
CFLAGS = -Wall -Werror -Wextra -std=c11
SOURCES = print.c
OBJECTS = $(SOURCES:.c=.o)
EXECUTABLE= make.exe
LIBA = libprint.a

all: $(SOURCES) $(EXECUTABLE)

$(EXECUTABLE): $(OBJECTS)
	$(CC) -L. -lprint $(OBJECTS) -o $@
.c:.o
	$(CC) -c $(CFLAGS) $< -o $@

static:
	ar -rs $(LIBA) $(OBJECTS)
	ranlib $(LIBA)
clean:
	rm -rf *.o $(EXECUTABLE)
rebuild:
	make clean
	make