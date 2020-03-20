PROGRAM = testappprojinfo
OBJECTS = $(addsuffix .o,$(PROGRAM))

CFLAGS = -g -Wall -Werror $(shell pkg-config proj --cflags)
LDFLAGS = $(shell pkg-config proj --libs)
EXPECTED_VERSION = $(shell pkg-config proj --modversion)

all: $(PROGRAM)

$(PROGRAM): $(OBJECTS)
	$(CC) -o $@ $< $(LDFLAGS)

clean:
	$(RM) $(PROGRAM) $(OBJECTS)

.PHONY: clean
