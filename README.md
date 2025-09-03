# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200=12                |   1205=24
|  1201=34                |   1206=68
|  1202=12
|  1203=34

#### Manual Calculations
![WhatsApp Image 2025-09-03 at 10 35 25_1573847e](https://github.com/user-attachments/assets/8e713e3a-f1f2-47de-929a-53d6daeddf38)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-03 at 10 34 10_f6c72fa4](https://github.com/user-attachments/assets/635bc523-e86f-4ad7-85db-03eb9796b0ae)

![WhatsApp Image 2025-09-03 at 10 21 16_fea55fa1](https://github.com/user-attachments/assets/0a1e2f65-229e-46df-a205-0d2401f6dae2)

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
![WhatsApp Image 2025-09-03 at 10 20 50_541d2766](https://github.com/user-attachments/assets/54d5b017-0fe8-43d8-a197-6e3bcca50a11)



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|    1200=12              |  1205=00
|    1201=34              |  1206=00
|    1202=12
|    1204=34

#### Manual Calculations

![WhatsApp Image 2025-09-03 at 10 35 27_7f82c022](https://github.com/user-attachments/assets/871841c7-b608-49a1-9986-61205ba74de4)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-03 at 10 22 38_f1551dbe](https://github.com/user-attachments/assets/63a6d5fa-aedd-42f6-a79c-e60e0254999b)

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|      1200=12            |  1204=44
|      1201=34            |  1205=51
|      1202=12            |  1206=97
|      1203=34            |  1207=0A

#### Manual Calculations

![WhatsApp Image 2025-09-03 at 10 35 26_c576804d](https://github.com/user-attachments/assets/25b2f3a8-8d50-4968-aea1-1309874de23b)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-03 at 10 34 28_d06a646c](https://github.com/user-attachments/assets/c67f60ae-7dae-42b9-878f-d289888a846e)

![WhatsApp Image 2025-09-03 at 10 32 13_bc6fcd31](https://github.com/user-attachments/assets/42bfb6c8-c436-47ce-b056-78b1922329ad)

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,1200H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200=12               |   1204=01
|   1201=34               |   1205=00         
|   1202=12               |
|   1203=34               |
#### Manual Calculations
![WhatsApp Image 2025-09-03 at 10 35 26_511442f5](https://github.com/user-attachments/assets/97eb0f37-037a-4e72-b3c9-d3fce3d4fcbb)


---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-03 at 10 39 23_b6acb2b7](https://github.com/user-attachments/assets/47af6679-789c-456d-b891-1f81511ecffe)

![WhatsApp Image 2025-09-03 at 10 32 52_baca1c42](https://github.com/user-attachments/assets/e6c80b8e-b798-4e31-a3e9-2c08ab001994)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
