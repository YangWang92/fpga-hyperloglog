# FPGA-based HyperLogLog Accelerator

## Build

Make sure Vivado 2019.1 is in your path = this is an example (your path might be different)
```
$ source /opt/Xilinx/Vivado/2019.1/settings64.sh
```

### Handling HLS IP cores

1. Setup build directory, e.g. for the hyperloglog module

```
$ cd hls/hyperloglog
$ mkdir build
$ cd build
$ cmake .. -DFPGA_PART=xcvu9p-flga2104-2L-e 
```

2. Run c-simulation
```
$ make csim
```

3. Run c-synthesis
```
$ make synthesis
```

4. Generate HLS IP core
```
$ make ip
```

5. Install HLS IP core in ip repository
```
$ make installip
```

After 'make installip' command the ip of the module could be found in ../iprepo 

## Contributors

- Amit Kulkarni amit.kulkarni@ieee.org
- Monica Chiosa monica.chiosa@inf.ethz.ch
- Thomas B. Preußer tpreusser@inf.ethz.ch
- Kaan Kara kaan.kara@outlook.com
- David Sidler david.sidler@microsoft.com
- Gustavo Alonso alonso@inf.ethz.ch

## Publication(s)
- A. Kulkarni, M.Chiosa, T.B.Preußer, K.Kara, D. Sidler, G. Alonso, 
*HyperLogLog Sketch Accleration on FPGA,* in FPL'20.

<a name="citation"></a>

## Citation

If you use the HyperLogLog Accelerator in your project please cite the following paper and/or link to the github project:

```
@INPROCEEDINGS{hll2020,
    author={A. Kulkarni and M. Chiosa and T. B. Preu{\ss}er and K. Kara and D. Sidler and G. Alonso}, 
    booktitle={FPL},
    year={2020}, 
    title={{HyperLogLog Sketch Acceleration on FPGA}}, 
}
```
