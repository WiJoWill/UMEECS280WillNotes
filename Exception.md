#### Exception

3 strategies for determining legitimate output for illegitimate input

- It's my problem
- I give up
- It's your problem

###### It's my problem

mldifying item or returning default output

###### I give up

abort() or exit()

###### It's your program

encode failure



#####Exception handling in C++

1. When code detects an error, it uses a throw statement
2. Code that might cause an error goes in a try{} block
3. Code that corrects an error goes in a catch{} block
4. If there is no code that corrects the error, the program exits.



Code that might cause an error goes in a **try{}** block.

Code that corrects an error goes in a **catch{}** block, goes immediately after the **try{}** block.