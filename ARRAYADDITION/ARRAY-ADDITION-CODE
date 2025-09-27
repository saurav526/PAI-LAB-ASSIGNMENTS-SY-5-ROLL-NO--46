section .text
global _start

_start:
    mov eax, x
    mov ebx, 0
    mov ecx, 5

top: 
    add bl, [eax]
    add eax, 1
    loop top

done:
    mov al, bl
    aam
    add ah, '0'
    add al, '0'
    mov [sum], ah
    mov [sum+1], al

display:
    mov edx, 2
    mov ecx, sum
    mov ebx, 1
    mov eax, 4
    int 0x80

    mov eax, 4
    mov ebx, 1
    mov ecx, newline    
    mov edx, 1
    int 0x80

    mov eax, 1
    int 0x80

section .data
x:
db 1 
db 2 
db 5
db 1 
db 2

newline db 10
sum db 0, 0
