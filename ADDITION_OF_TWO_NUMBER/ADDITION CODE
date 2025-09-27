global _start

section .data

sum db 0
newline db 10

section .text

_start:

mov eax,8
mov ebx,1
add eax, ebx
add eax,48 ;ASCII representation
mov [sum],eax
int 80h

mov eax,4
mov ebx,1
mov ecx,sum
mov edx,1
int 80h

mov eax,4
mov ebx,1
mov ecx,newline
mov edx,1
int 80h

mov eax,1
xor ebx,ebx
int 80h
