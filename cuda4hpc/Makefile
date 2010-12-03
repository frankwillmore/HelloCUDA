#!/usr/bin/make

############################################################
#                                                          # 
#      Introduction to CUDA for HPC Makefile               #
#                                                          # 
#      (C) 2010 Texas Advanced Computing Center            # 
#                                                          # 
############################################################

CC=nvcc
CFLAGS-DEBUG= -G -g -O0 -lcudart 
CFLAGS-EMU= -deviceemu
CFLAGS= -lcudart

shift:	shift.cu
	$(CC) $(CFLAGS) shift.cu -o shift

debug:	shift.cu
	$(CC) $(CFLAGS-DEBUG) shift.cu -o shift 

emu:	shift.cu
	$(CC) $(CFLAGS-EMU) shift.cu -o shift 

clean:
	rm -f shift 

