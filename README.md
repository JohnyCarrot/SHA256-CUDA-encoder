# SHA256CUDA

This program is supposed to encode any text to SHA256 hash starting with n zeros.

Enter a message - here you type your text
Nonce - Starting nonce value
Difficulty - number of zeros
result_count - set a tolerance for lower difficulty. For example if result_count is 2 and difficulty is 10 and hash with 9 zeros is found, then this hash (with nonce)                will be displayed. Default is 1.





Example run:


```
Admin:~/src/cuda/SHA256CUDA/SHA256CUDA$ ./hash_test 
Enter a message : Hello, world
Nonce : 0
Difficulty : 7

result_count : 1
Shared memory is 16KB
Result_Difficulty_Number:7
47449.4 8388608
176790 hash(es)/s
Nonce : 8388608
2050.079200 310378496
151398304 hash(es)/s
Nonce : 318767104
Hello, world525573496

0000000ce558a4bebb06f7dc5711897d3aeb38acad0b260311cadfd7bf8b628b

Admin:~/src/cuda/SHA256CUDA/SHA256CUDA$ echo -n Hello, world525573496 | sha256sum
0000000ce558a4bebb06f7dc5711897d3aeb38acad0b260311cadfd7bf8b628b  -

