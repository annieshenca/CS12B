#------------------------------------------
#Makefile for hello.o with Macros
#------------------------------------------

FLAGS	 = -std=c99 -Wall
SOURCES  = charType.c
OBJECTS  = charType.o
EXEBIN   = charType
OUTPUT   = leakCheck

all: $(EXEBIN)

$(EXEBIN) : $(OBJECTS)
	gcc -o $(EXEBIN) $(OBJECTS)

$(OBJECTS) : $(SOURCES)
	gcc -c $(FLAGS) $(SOURCES)

clean:
	rm $(EXEBIN) $(OBJECTS)

check:
	valgrind --leak-check=full $(EXEBIN) $(SOURCES) $(OUTPUT)
