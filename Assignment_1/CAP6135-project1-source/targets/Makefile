# tools
CC := gcc
RM := rm -f

# flags
# the flag -fno-stack-protector is used to disable "stackGuard" protection.
# the flag -z execstack is used to disable "non executable stack" default protection 
# so that the shellcode in stack memory can be executed.
CFLAGS := -ggdb -fno-stack-protector -z execstack 
LDFLAGS :=
LDLIBS :=

# sources
sources := target.c
targets := target

# gmake magic
.PHONY: default all clean

#targets
default: all
all: $(targets)

clean:
	$(RM) $(targets) $(sources:.c=.o)
