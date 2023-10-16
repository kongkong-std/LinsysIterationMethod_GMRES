# sequential implementation
CC = gcc
CMD = -g -Wall -O0
CFLAGS = -c
SRC = ../src
LIB_FLAG = -lm
LIB = $(LIB_FLAG)

OBJECT := $(patsubst %.c,%.o,$(wildcard $(SRC)/*.c))

.PHONY: all clean

all: app_exe

app_exe: $(OBJECT)
	$(CC) $(CMD) -o app_exe $(OBJECT) $(LIB)

%.o: %.c
	$(CC) $(CFLAGS) $(CMD) "$<" -o "$@"

clean:
	rm app_exe $(OBJECT)