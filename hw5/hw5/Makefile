# Lines starting with # are comments

# Some variable definitions to save typing later on
CC = gcc
CFLAGS = -std=c99 -Wall -Wextra -pedantic -g

# Default (first) target -- fill this in
hw5: hw5.o prompts.o methods.o
	$(CC) $(CFLAGS) -o hw5 hw5.o prompts.o methods.o

# Links the test executable
unittest: unittest.o prompts.o methods.o
	$(CC) $(CFLAGS) -o unittest unittest.o prompts.o methods.o

# Compiles hw5.c into an object file
hw5.o: hw5.c prompts.h methods.h
	$(CC) $(CFLAGS) -c hw5.c

# Compiles prompts.c into an object file
prompts.o: prompts.c prompts.h
	$(CC) $(CFLAGS) -c prompts.c
	
methods.o: methods.c methods.h prompts.h
	$(CC) $(CFLAGS) -c methods.c

# Compiles unittest.c into an object file
unittest.o: unittest.c methods.h prompts.h
	$(CC) $(CFLAGS) -c unittest.c

# 'make clean' will remove intermediate & executable files
clean:
	rm -f *.o unittest hw5

