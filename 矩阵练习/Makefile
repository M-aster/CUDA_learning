.PHONY:clean all

CFLAGS = -O3 -DUSE_DP -allow-unsupported-compiler

all:matrix

matrix:matrix.cu	
	nvcc ${CFLAGS} matrix.cu -o matrix

# clean:
#     rm -rf matrix