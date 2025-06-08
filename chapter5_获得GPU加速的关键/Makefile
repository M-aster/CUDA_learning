all: add1cpu add2gpu add3memcpy arithmetic1cpu arithmetic2gpu

add1cpu: add1cpu.cu
	nvcc -O3 -DUSE_DP -allow-unsupported-compiler add1cpu.cu -o add1cpu

add2gpu: add2gpu.cu
	nvcc -O3 -DUSE_DP -allow-unsupported-compiler add2gpu.cu -o add2gpu

add3memcpy: add3memcpy.cu
	nvcc -O3 -DUSE_DP -allow-unsupported-compiler add3memcpy.cu -o add3memcpy

arithmetic1cpu: arithmetic1cpu.cu
	nvcc -O3 -DUSE_DP -allow-unsupported-compiler arithmetic1cpu.cu -o arithmetic1cpu

arithmetic2gpu: arithmetic2gpu.cu
	nvcc -O3 -DUSE_DP -allow-unsupported-compiler arithmetic2gpu.cu -o arithmetic2gpu

.PHONY: clean

clean:
	rm -rf add1cpu add2gpu add3memcpy arithmetic1cpu arithmetic2gpu
