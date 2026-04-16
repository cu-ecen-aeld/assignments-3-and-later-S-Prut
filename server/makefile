TARGET  := aesdsocket
SOURCES := aesdsocket.c
OBJECTS := $(SOURCES:.c=.o)

CC := $(CROSS_COMPILE)gcc
CFLAGS += -Wall -Werror

Debug: all
default: all
all: $(TARGET)
	@echo "Compiler: " $(CC)

# generic rule to make objects files from C source files
.c.o:
	@echo "--- start compile sources" $< " ---"
	$(CC) $(CFLAGS) -c $^ -o $@
	@echo "--- end compile sources" $< " ---"

$(TARGET): $(OBJECTS)
	@echo "--- start build target" $@ " ---"
	$(CC) $(OBJECTS) -o $@
	@echo "--- end build target" $@ " ---"

.PHONY: clean
cleanDebug: clean
clean:
	rm -f $(TARGET) ./*.o
