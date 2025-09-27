global _start

section .data
msg1 db "Enter the 1st Value: ",10
len1 equ $-msg1

msg2 db "Enter the 2nd Value: ",10
len2 equ $-msg2

msg3 db "The subtraction is: "
len3 equ $-msg3

newline db 10

section .bss
val1 resb 2
val2 resb 2
result resb 2

section .text
_start:

    ; print msg1
    mov eax,4
    mov ebx,1
    mov ecx,msg1
    mov edx,len1
    int 0x80

    ; read val1
    mov eax,3
    mov ebx,0
    mov ecx,val1
    mov edx,2
    int 0x80

    ; print msg2
    mov eax,4
    mov ebx,1
    mov ecx,msg2
    mov edx,len2
    int 0x80

    ; read val2
    mov eax,3
    mov ebx,0
    mov ecx,val2
    mov edx,2
    int 0x80

    ; convert ascii -> number
    mov al,[val1]
    sub al,'0'
    mov bl,[val2]
    sub bl,'0'

    ; subtraction: val1 - val2
    sub al,bl

    ; convert number -> ascii
    add al,'0'

    ; store result
    mov [result],al

    ; print msg3
    mov eax,4
    mov ebx,1
    mov ecx,msg3
    mov edx,len3
    int 0x80

    ; print result
    mov eax,4
    mov ebx,1
    mov ecx,result
    mov edx,1
    int 0x80

    ; print newline
    mov eax,4
    mov ebx,1
    mov ecx,newline
    mov edx,1
    int 0x80

    ; exit
    mov eax,1
    xor ebx,ebx
    int 0x80
