#Tic-Tac-Toe

This is the second assignment of the course DD2380 Artificial Intelligence

## Compile

```
g++ *.cpp -Wall -o TTT
```

## Run
The players use standard input and output to communicate
The Moves made are shown as unicode-art on std err if the parameter verbose is given

### Play against self in same terminal

```
mkfifo pipe
./TTT init verbose < pipe | ./TTT > pipe
```

### Play against self in two different terminals
#### Terminal 1:
```
mkfifo pipe1 pipe2
./TTT init verbose < pipe1 > pipe2
```

#### Terminal 2:

```
./TTT verbose > pipe1 < pipe2
```

### Play against your friend (in the same terminal)
If you want two algorithms to play against each other, create two folders, folder1 and folder2. Copy the skeleton to both of these folders and compile the code. Then run:

```
mkfifo pipe
./folder1/TTT init verbose < pipe | ./folder2/TTT > pipe
```


