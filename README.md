```asm
section .data
    name db 'André Duarte', 0
    languages db 'Assembly for x86_64, RISC-V and ARMv7/ C/C++/Python/', 0
    description db 'I love writing in low-level languages but I adore pytorch and Transformers', 0

section .bss
    reservedSpace resb 100

section .text
    global _start

_start:
    ; allocate memory space
    mov eax, 45
    mov ebx, 100
    int 0x80
    mov [reservedSpace], eax

    ; copy name to memory space
    mov eax, 4
    mov ebx, [reservedSpace]
    mov ecx, name
    mov edx, 12
    int 0x80

    ; copy languages to memory space
    mov eax, 4
    mov ebx, [reservedSpace]
    mov ecx, languages
    mov edx, 30
    int 0x80

    ; copy description to memory space
    mov eax, 4
    mov ebx, [reservedSpace]
    mov ecx, description
    mov edx, 60
    int 0x80

    ; release memory space
    mov eax, 46
    mov ebx, [reservedSpace]
    int 0x80

    ; exit
    mov eax, 1
    xor ebx, ebx
    int 0x80
```
