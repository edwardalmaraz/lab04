## Description of Bugs Encountered

Overall the lab was a success however there was certain issues in correctly identifying the correct ports to wire for the cpumemory. After reading over the different ports available in the cpumemory, I was able to sort out each connection and properly wire the cpumemory module. Another issue that I encoutered while wiring was that I was directly connecting tunnels to output ports. This caused issues because you cannot do that in Digital. Instead you need to use a wire to connect the port entry and the tunnel together. If not, then Digital will think that you have a loose tunnel and that in itself will create some errors. 

Another issue that I had was that I was hardcoding values such as 4 and 2 that were fed into ALU B and ALU control respectively. However, I failed to correctly set the correct amount of bits to hold the value so that caused the ports to storing incorrect values. 


## Hand Tracing
(Assuming that we only translate to binary as mentioned in lab) 
```asm
and $t0 $t1 $t2
addi $t3 $t4 123
lw $t5, 135($t1)
sw $t3, 136($t1)
beq $t3, $zero, -10
```

1) 000000 01001 01010 01000 00000 100100
2) 001000 01100 01011 0000000001111011
3) 100011 01001 01101 0000000010000111
4) 101011 01001 01011 0000000010001000
5) 000100 01011 00000 1111111111110110