CFLAGS=-O3 -mcpu=cortex-a8 -mfpu=neon -std=c99 -Wall -Wextra -pedantic -Wno-long-long

all: check bench

debug:
	@$(CC) $(CFLAGS) -o debug ../../utils/debug.c ../../utils/io.c opp.c
	@./debug
	@rm debug

bench:
	@$(CC) $(CFLAGS) -o bench ../../utils/bench.c opp.c
	@./bench
	@rm bench

check:
	@$(CC) $(CFLAGS) -I../ -o check ../../utils/check.c opp.c
	@./check
	@rm check
