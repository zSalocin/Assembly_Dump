MVI B,15

loopExt: LXI H,0850H
MOV C,B

loopInter: MOV A,M
INX H
MOV D,M
CMP D
JC skip
MOV M,A
DCX H
MOV M,D
INX H
skip:DCR C
JNZ loopInter

DCR B
JNZ loopExt