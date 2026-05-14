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
|       1200🔢       01         12

|         1200                    |

#### Manual Calculations

(Add your calculation here)

---
<img width="1307" height="1086" alt="WhatsApp Image 2026-05-14 at 9 46 32 AM" src="https://github.com/user-attachments/assets/b156eee4-7679-41f6-93d1-defd4d941894" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="650" height="452" alt="WhatsApp Image 2026-05-14 at 9 47 00 AM" src="https://github.com/user-attachments/assets/7a408033-263e-47a2-873a-1d9804722abb" />


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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
<img width="1600" height="868" alt="WhatsApp Image 2026-05-14 at 10 13 46 AM" src="https://github.com/user-attachments/assets/23fdde02-e44f-4477-809a-845e6b24903d" />
<img width="1430" height="453" alt="image" src="https://github.com/user-attachments/assets/fc3a26ee-2490-4516-b5ac-5c3f23760313" />



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="648" height="433" alt="image" src="https://github.com/user-attachments/assets/751881b6-6b6e-414c-9537-3430f82b4d69" />



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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
<img width="1600" height="1139" alt="WhatsApp Image 2026-05-14 at 10 14 59 AM" src="https://github.com/user-attachments/assets/a4fb030e-ec8c-4b22-ab4c-447d6d90dc40" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="641" height="426" alt="WhatsApp Image 2026-05-14 at 10 15 20 AM" src="https://github.com/user-attachments/assets/e349078a-5e4d-4383-9e39-45f5ff3dd87a" />


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
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
<img width="1600" height="1338" alt="image" src="https://github.com/user-attachments/assets/1890fa82-8dba-4479-a0b9-4dafb517029d" />

## OUTPUT FROM MASM SOFTWARE
<img width="643" height="430" alt="image" src="https://github.com/user-attachments/assets/498b071f-2c0e-4fc4-b856-af00073d08f0" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

