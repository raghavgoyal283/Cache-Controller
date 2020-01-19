# Cache-Controller

WHAT IS A CACHE CONTROLLER:

Cache Controller is a hardware which acts as an intermediate between the processor and the cache memory. It executes the read and write requests from the processor and copies or replaces data within different levels of cache memory and main memory to reduce the average time taken by the processor to retrieve data from an address

ABOUT THE PROJECT:
Here in this project, we have implemented a Cache Controller for two layers of Cache Memory. The L1 Cache  Memory is Direct Mapped and the mapping used for L2 Cache is four-way set associative. The Cache Controller performs read or write instructions on the address location issued by the processor and outputs a signal indicating Cache hit or miss. In direct mapping, each line in the next memory level ( L2 Cache here) is mapped to a specific line in the Cache (L1 Cache here). Direct Mapping being the simplest mapping policy is easiest to implement but has some disadvantages such as if two memory blocks which map to the same line in Cache are continuously referred, then the two blocks are continuously swapped in the Cache Memory.

Note: 
a) Read the 'Inportant_Must_Read_First' to understand the overall structure of the project and the relevance of the files included
b) Read the 'Module_Explanation' file to understand in detail about the different modules included in the verilog project
c) The code in the verilog files has been well commented to specify the tasks being achieved through different blocks of code


ALGORITHMS AND POLICIES USED:
a) No-Write Allocate Policy:
In no-write allocate policy, when a write miss occurs in a lower level of cache memory, the data is updated in the higher level of cache memory or in main memory (wherever found), but is not loaded into the lower level cache memory.
b) Least Recently Used Algorithm:
LRU Replacement Algorithm works on the idea that a block of memory that has been heavily used in the last few instructions is likely to be used again in the next few instructions. Thus, the memory block lying unused for the longest time is thrown out whenever required. 
c)Write-Back Policy
In write-back policy, the data is updated in a cache level every time a write instruction is issued by the processor, but it is written into higher levels of cache or main memory only when the memory block evicts from the lower cache level.

FEATURES:
Issues wait signals of appropriate durations for different Cache levels, efficiently allocates data using the above mentioned algorithms and policies, prevent losses during data movement between the Cache memory and Main Memory.


IMPLEMENTATION ON BASYS 3 FPGA:
The Verilog Code was also implemented on the Basys 3 Artix-7 FPGA (Field Programmable Logic Array) Board to test it for different combinations of inputs. 


