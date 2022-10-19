# Змінна 'CC' вказує на компілятор, який буде використовуватись для збірки
CC=g++

# Змінна 'CFLAGS' містить прапори, які передаються компілятору
CFLAGS=-c -Wall

all: task

task: main.o factorial.o hello.o
	$(CC) main.o factorial.o hello.o -o MakefileApp
	
main.o: main.cpp
	$(CC) $(CFLAGS) main.cpp

factorial.o: factorial.cpp
	$(CC) $(CFLAGS) factorial.cpp

hello.o: hello.cpp
	$(CC) $(CFLAGS) hello.cpp

clean:
	rm -rvf *.o MakefileApp
.PHONY: clean