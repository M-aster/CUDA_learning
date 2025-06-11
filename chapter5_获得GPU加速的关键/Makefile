.PHONY:all clean

targets=add1cpu add2gpu add3memcpy arithmetic1cpu arithmetic2gpu
CFLAGS = -O3 -DUSE_DP -allow-unsupported-compiler
sources=add1cpu.cu add2gpu.cu add3memcpy.cu arithmetic1cpu.cu arithmetic2gpu.cu
objects=add1cpu add2gpu add3memcpy arithmetic1cpu arithmetic2gpu

all:$(targets)

add1cpu: add1cpu.cu
	nvcc $(CFLAGS) add1cpu.cu -o add1cpu

add2gpu: add2gpu.cu
	nvcc $(CFLAGS) add2gpu.cu -o add2gpu

add3memcpy: add3memcpy.cu
	nvcc $(CFLAGS) add3memcpy.cu -o add3memcpy

arithmetic1cpu: arithmetic1cpu.cu
	nvcc $(CFLAGS) arithmetic1cpu.cu -o arithmetic1cpu

arithmetic2gpu: arithmetic2gpu.cu
	nvcc $(CFLAGS) arithmetic2gpu.cu -o arithmetic2gpu
# $(targets):$(sources)
# 	nvcc $(CFLAGS) $(sources) -o $(targets)

clean:
	rm -rf add1cpu.exe add2gpu.exe add3memcpy.exe arithmetic1cpu.exe arithmetic2gpu.exe
