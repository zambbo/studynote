# Stack

## what does the stack do

>- Saving some register values
>- Saving **return address**
>- Passing of data
>- Allocating space for local variables and deallocating them

## %rsp register

- Pointing top address of the stack
### pushq src
1. Decrement %rsp by 8bits (stack grows downwards)
2. Fetch operand at src and write it at address given by %rsp

### popq dest
1. Read operand at address given by %rsp
2. Increment %rsp by 8bits

### call
1. push return address to the stack
2. jump to the target

> 1. Save %rip(pointing next address) to stack
> 2. change %rip to target address

