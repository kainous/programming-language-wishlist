# Optimizations
## Opt T
The optional type should optimize based on one of 2 situations:
* If the object is placed on the heap, then the None case is handled as a null-pointer
* If the object is maintained in the stack or in registers, it's handled as a tuple of Boolean and Value (i.e. the Boolean serves as a Type-Marker for the Discriminated Union)

