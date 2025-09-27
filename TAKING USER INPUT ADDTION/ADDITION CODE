global _start
msg1 db "Enter the 1st Value: ",10
len1 equ $-msg1

msg2 db "Enter the 2nd Value: ",10
len2 equ $-msg2

msg3 db "The addition is: "
len3 equ $-msg3

newline db 10

section .bss
val1 resb 2
val2 resb 2
result resb 2

section .text
_start:

mov eax,4
mov ebx,1
mov ecx,msg1
mov edx,len1
int 0x80

mov eax,3
mov ebx,0
mov ecx,val1
mov edx,2
int 0x80

mov eax,4
mov ebx,1
mov ecx,msg2
mov edx,len2
int 0x80

mov eax,3
mov ebx,0
mov ecx,val2
mov edx,2
int 0x80

mov al,[val1]
sub al,'0'
mov bl,[val2]
sub bl,'0'

add al,bl
add al,'0'

mov [result],al

mov eax,4
mov ebx,1
mov ecx,msg3
mov edx,len3
int 0x80

mov eax,4
mov ebx,1
mov ecx,result
mov edx,1
int 0x80

mov eax, 4
mov ebx, 1
mov ecx, newline    
mov edx,1
int 0x80

mov eax,1
xor ebx,ebx
int 0x80
