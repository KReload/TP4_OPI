CC= gcc
CFLAGS= -O3 -Wall -funroll-loops
LDLIBS= -lpng
PROGRAMMES= pbm2eps9 pbm2png

all: pbm2png pbm2eps9

pbm2png: pbm2png.c
	$(CC) $(CFLAGS) -s -o pbm2png pbm2png.c $(LDLIBS)
pbm2eps9: pbm2eps9.o printer.o 

	$(CC) -s -o pbm2eps9 pbmeps9.o printer.o

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $< $(LDLIBS)

clean:
	rm -f $(PROGRAMMES) *.o

.PHONY: all clean
