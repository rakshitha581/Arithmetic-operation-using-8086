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
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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
| ----------------------- | -----------------------  |
| 1200 12                 | 1204 24                  |
| 1201 34                 | 1205 68                  |
| 1202 12                 | 1206 00                  |
| 1203 34                 | 1207 C4                  |

#### Manual Calculations
![add ](https://github.com/user-attachments/assets/6429a5b4-5e66-4202-b7b0-23d74ae5b9b3)



---

## OUTPUT IMAGE FROM MASM SOFTWARE
![add asm](https://github.com/user-attachments/assets/f2b1d6ba-4530-40a4-94cb-90b8ea966f2e)
![add output](https://github.com/user-attachments/assets/4ae3833f-73a6-4dc1-b059-daf89f8934da)

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
MOV SI,1200H
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
| 1200 12                 | 12024 00                 |
| 1201 34                 | 1205  00                 |
| 1202 12                 | 1206  00                 |
| 1203 34                 | 1207  C4                 |

#### Manual Calculations

![sub](https://github.com/user-attachments/assets/cd2b98e3-e40e-44ed-935f-850f872b6f13)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
![sub asm](https://github.com/user-attachments/assets/320fd842-0585-40e9-b7ed-6b715638ff20)
![sub output](https://github.com/user-attachments/assets/e8e0588d-3616-42de-8c1d-35ace4f63046)

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
| 1200 12                 | 1204 44                  |
| 1201 34                 | 1205 51                  |          
| 1202 12                 | 1206 97                  |
| 1203 34                 | 1207 0A                  |
#### Manual Calculations
![mul](https://github.com/user-attachments/assets/13ff685c-4991-4bf0-977f-5da40674dd56)



---

## OUTPUT SCREEN FROM MASM SOFTWARE
![mul asm](https://github.com/user-attachments/assets/aafb3b79-0189-421e-adf6-28858f6c1df0)
![mul output](https://github.com/user-attachments/assets/83998e7d-e078-4c2c-aa0f-b1ac0c97a10d)

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
| 1200 12                 | 1204 01                  |
| 1201 34                 | 1205 00                  |
| 1202 12                 | 1206 00                  |
| 1203 34                 | 1207 00                  |
#### Manu|al Calculations
![div](https://github.com/user-attachments/assets/323842ef-35d0-4b8d-b7b0-9e3fcb32ab63)



---
## OUTPUT FROM MASM SOFTWARE

![div asm](https://github.com/user-attachments/assets/a1cc1545-0162-4477-8433-87658710c35b)
![div output](https://github.com/user-attachments/assets/3c0afef7-5364-4955-a22e-48753e8fb735)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
