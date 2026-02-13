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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200              |           01             |
|       1201              |           13             |

#### Manual Calculations
![WhatsApp Image 2026-02-09 at 11 29 05 AM](https://github.com/user-attachments/assets/54f1050a-dbe0-4396-b5d9-bae1ae72d0de)



---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2026-02-07 at 9 32 31 AM (1)](https://github.com/user-attachments/assets/a3da2d63-d5e3-4260-8a96-97d7d7a05c89)


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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200            |          10              |
|         1210            |          11              |

#### Manual Calculations

![WhatsApp Image 2026-02-09 at 11 29 25 AM](https://github.com/user-attachments/assets/061d5b0d-ffbf-4c9c-8660-36ba41fd59b9)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2026-02-07 at 9 35 17 AM](https://github.com/user-attachments/assets/f9c44623-3ee6-4d5c-b71f-069edc28f955)


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
MOV SI,2000H
MOV DX,0000H
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
|         1200            |           42             |
|         1210            |           81             |
#### Manual Calculations

![WhatsApp Image 2026-02-09 at 11 29 39 AM](https://github.com/user-attachments/assets/78e94844-a0f5-4cb9-bcbb-a6bf33a8c829)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2026-02-07 at 9 44 29 AM](https://github.com/user-attachments/assets/5d77e940-dbf6-4564-b573-634ca216e1a6)


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
MOV SI,2000H
MOV DX,0000H
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
|         1200            |           01             |
|         1210            |           00             |

#### Manual Calculations

![WhatsApp Image 2026-02-09 at 11 29 52 AM (1)](https://github.com/user-attachments/assets/750fc0e5-c326-497d-a1f7-800e59e34082)


---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2026-02-09 at 10 20 14 AM](https://github.com/user-attachments/assets/08b58841-dd06-431f-927e-a008bfd7adba)




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

