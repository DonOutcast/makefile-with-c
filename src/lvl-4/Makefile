.PHONY: clean, rebuild
CC = gcc
CFLAGS = -Wall -Werror -Wextra -std=c11
SOURCES = print.c
OBJECTS = $(SOURCES:.c=.o)
EXECUTABLE= make.exe

all: $(SOURCES) $(EXECUTABLE)

$(EXECUTABLE): $(OBJECTS)
	$(CC) $(OBJECTS) -o $@
.c:.o
	$(CC) $(CFLAGS) $< -o $@
clean:
	rm -rf *.o $(EXECUTABLE)
rebuild:
	make clean
	make