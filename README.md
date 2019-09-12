# squirrel-amalgamation
1. it's squirrel lanaguage with some little change,and combine all source code files to one file.
2. the code base squirrel 3.1, include 'squirrel' and 'stdlib'.
3. add keyword 'var', 'var' is the same function with keywoed 'local'.
4. add 2 opcode in VM, used for direct memory read/write, it's not a good ideal for a script lanaguage,but it's useful.
   add inner function malloc/free,used for alloc/free memory,it's direct call C malloc/free function,no RC,no RC,no RC,must mannul alloc  and delete memeory.
   add grammar [ptr]@[u8|u16|u24|u32|bu16|bu24|bu32|int|float|double|char]|[idx] ,you can direct access memory as C/C++.
   eg: var ptr=malloc(1024);ptr@u32=0x11223344;print(format("0x%x",ptr@u16[2]));free(ptr);
