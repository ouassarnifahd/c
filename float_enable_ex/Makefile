CC			= gcc
CFLAGS		= -c -g -Wall -D_GNU_SOURCE -std=gnu99 -Wall -Wextra #suppress main.c:8: error: ‘for’ loop initial declarations are only allowed in C99 mode
LDFLAGS		= -lpthread -lm
SOURCES		= main.c
INCLUDES	= -I.
OBJECTS		= $(SOURCES:.c=.o)
TARGET		= float_enable_ex

all: $(SOURCES) $(TARGET)

$(TARGET): $(OBJECTS) 
	$(CC) $(LDFLAGS) $(OBJECTS) -o $@

.c.o:
	$(CC) $(CFLAGS) $(INCLUDES) $< -o $@

.PHONY:
clean:
	rm -rf $(OBJECTS) $(TARGET)
