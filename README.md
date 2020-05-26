Make sure Vivado 2019.1 is in your path = this is an example (your path might be different)
```
$ source /opt/Xilinx/Vivado/2019.1/settings64.sh
```


## Handling HLS IP cores

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

5. Instal HLS IP core in ip repository
```
$ make installip
```

After 'make installip' command the ip of the module could be found in ../iprepo 